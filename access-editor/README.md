#  <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/logo-onv.png?raw=true" align="left" height="80" width="200" > Observatoire National Ventilation <br>Guide d'utilisation pour l'accès éditeur

1. [Création de compte éditeur](#creation)
2. [API Reference](#apiReference)
    1. [Authentification logiciel – Observatoire National Ventilation](#authentification)
    2. [Comptes opérateurs](#comptes)
    3. [Environnement de test](#testEnv)
    4. [API](#api)
    5. [Description des Erreurs](#errors)

----

L'Observatoire National Ventilation propose une API permettant l'intégration avec des logiciels tiers.

## 1. Création de compte éditeur <a name="creation"></a>

Pour pouvoir utiliser l'API de l'Observatoire, il est nécessaire de créer un compte Editeur.

Pour créer votre compte Editeur, rendez-vous sur l'Observatoire National Ventilation, cliquez sur le bouton "Connexion", puis en bas de la page, cliquez sur le bouton "Créer un compte éditeur".

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/create_editor_compte.png?raw=true" alt="Création de compte utilisateur">
</kbd>
<br/><br/>

Remplissez ensuite le formulaire en renseignant toutes les informations demandées. Vous recevrez alors un email généré automatiquement par l’Observatoire National Ventilation pour valider la création de votre compte éditeur et choisir votre mot de passe pour sécuriser l'accès à votre compte.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/set_password.png?raw=true" alt="Créer votre mot de passe">
</kbd>
<br/><br/>

## 2. API Reference <a name="apiReference"></a>

L'API de l'Observatoire National Ventilation est une API REST.

### i.  Authentification logiciel – Observatoire National Ventilation <a name="authentification"></a>

L'API de l'Observatoire National Ventilation utilise des clés secrètes pour authentifier les requêtes provenant des logiciels. 
 - Pour obtenir votre clé secrète, connectez-vous à votre compte éditeur sur l'Observatoire et rendez-vous dans le menu Compte > Mon application

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/generate_secret_key.png?raw=true" alt="Générer une clé secrète">
</kbd>
<br/><br/> 

Cliquez alors sur le bouton "Générer la clé secrète" pour obtenir la clé secrète de votre application.

**Attention: c'est la seule fois où votre clé secrète sera affichée. Veillez à la sauvegarder immédiatement de manière sécurisée. Il ne sera ensuite plus possible de l'afficher.**

L'authentification est réalisée via HTTP Basic Auth. Dans les requêtes envoyées à l'API, spécifiez votre nom de logiciel comme nom d'utilisateur Basic Auth et votre clé secrète comme mot de passe.

### ii. Comptes opérateurs<a name="comptes"></a>

Vous devez spécifier le compte de l'opérateur qualifié pour lequel les requêtes sont effectuées. Ajoutez le Header ``Account`` à vos requêtes en spécifiant l'identifiant du compte.

**Nota : Pour l’obtention de l’identifiant du compte, se rapprocher de l’opérateur reconnu. L'utilisateur doit avoir activé son compte sur l'Observatoire.**

Vous devez spécifier la "authorization-key", la clé utilisée pour identifier l'opérateur et le logiciel qu'il utilise en ajoutant le header ``authorization-key`` à vos requêtes. Cette clé est générée par l'ONV lors de l'autorisation et doit être sauvegardée sur le logiciel utilisé.

**Nota : Si le logiciel ne dispose pas encore d’autorisation pour cet utilisateur, ce header doit quand même être présent avec la valeur "". Si une nouvelle demande est réalisée pour un même utilisateur, son authorization-key sera différente**

Vous pouvez utiliser la route ``/ext/ventilation-reports/test-access`` pour vérifier l'autorisation d'accès de votre logiciel à un compte utilisateur.

```Bash
curl --location "https://www.observatoire-national-ventilation.developpement-durable.gouv.fr/ext/ventilation-reports/test-access" -u "nom_logiciel:cle_secrete" --header "Account: user" --header "Accept-Language: fr" --header "SoftwareVersion: 1.0" --header "authorization-key;" --header "Accept: application/json" -v
```

L'utilisateur (opérateur reconnu) doit avoir autorisé votre logiciel à effectuer des actions sur son compte.

Lors de la première requête pour un compte, l'API retourne une réponse ``401`` et fournit un header ``GrantAccessUrl`` qui contient comme valeur une URL à présenter à l'opérateur pour lui permettre d'autoriser l'accès de votre application à son compte. Vous pouvez également trouver l'en-tête ``authorization-key``, qui doit être enregistrée par le logiciel utilisant l'API et envoyée dans l'en-tête pour toutes les demandes ultérieures de l'opérateur.

Exemple :


```Bash
curl --location "https://www.observatoire-national-ventilation.developpement-durable.gouv.fr/ext/ventilation-reports/test-access" -u "nom_logiciel:cle_secrete" --header "Account: user" --header "Accept-Language: fr" --header "SoftwareVersion: 1.0" --header "authorization-key;" --header "Accept: application/json" -v
HTTP/1.1 401 Unauthorized`
Server: nginx/1.21.3`
Date: Thu, 07 Jul 2022 10:28:04 GMT`
Content-Length: 0`
Connection: keep-alive`
Expires: 0`
GrantAccessUrl: http://www.observatoire-national-ventilation.developpement-durable.gouv.fr/software-authorization/259/grant-access`
authorization-key: dsWYDvnkvU8jHOD2yClv`

{
  "timestamp" : "2024-07-11T12:57:48.807+00:00",
  "status" : 401,
  "error" : "Unauthorized",
  "path" : "/ext/ventilation-reports/test-access"
}
```

En ouvrant l'url ``GrantAccessUrl`` dans son navigateur, l'opérateur s'authentifie et peut ensuite valider ou refuser la demande d'accès du logiciel à son compte.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/grant-access.png?raw=true" alt="Accorder l'accès au logiciel">
</kbd>
<br/><br/>

Après validation de l'accès, votre application peut effectuer des requêtes pour le compte de cet opérateur :

```Bash
curl --location "https://www.observatoire-national-ventilation.developpement-durable.gouv.fr/ext/ventilation-reports/test-access" -u "nom_logiciel:cle_secrete" --header "Account: user" --header "Accept-Language: fr" --header "SoftwareVersion: 1.0" --header "authorization-key: dsWYDvnkvU8jHOD2yClv" --header "Accept: application/json" -v
HTTP/1.1 200 OK
```

### iii. Environnement de test <a name="testEnv"></a>

Pour tester l'intégration de votre logiciel avec l'Observatoire National Ventilation, trois utilisateurs de test ont automatiquement été créés lors de la création de votre compte éditeur.

|Login||
|---|---|
|*nomDuLogiciel*_test_pending|utilisateur n'ayant ni validé ni approuvé l'accès de votre logiciel à son compte|
|*nomDuLogiciel*_test_accepted|utilisateur ayant accepté l'accès de votre logiciel à son compte|
|*nomDuLogiciel*_test_refused|utilisateur ayant refusé l'accès de votre logiciel à son compte|

*nomDuLogiciel* est à remplacer par le nom de votre logiciel renseigné lors de la création de votre compte.

> Exemple : si votre logiciel s'appelle "MyVentilationSoftware", l'utilisateur de test ayant accepté l'accès de votre logiciel à son compte a pour login "MyVentilationSoftware_test_accepted".

**Nota : Vous devez définir la valeur de ``authorization-key`` : ``MO9jxDxlqYWbVERjprkg`` dans toutes les requêtes pour ces trois comptes de test.**

Vous pouvez tester l'intégration de votre logiciel en utilisant les routes de l'API avec ces trois utilisateurs. Les éventuelles données publiées pour ces utilisateurs n'auront pas d'impact sur les données utilisées pour les statistiques de l'Observatoire National Ventilation.

```Bash
curl https://www.observatoire-national-ventilation.developpement-durable.gouv.fr/ext/test-access -u MyVentilationSoftware:cle_secrete -H "Account:MyVentilationSoftware_test_accepted" -H "authorization-key:MO9jxDxlqYWbVERjprkg" --header "Accept-Language: fr" --header "SoftwareVersion: 1.0" --header "Accept: application/json" -v
HTTP/1.1 200 OK
```

### iv. API <a name="api"></a> 
La documentation détaillée des actions disponibles via l'API est disponible [sur cette page de l'Observatoire National Ventilation](https://www.observatoire-national-ventilation.developpement-durable.gouv.fr/editor/docs).

<br/><br/>
<a href="#top"> <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/arrow_top.png?raw=true"  height="10" width="20" alt="Haut de page">HAUT DE PAGE</a> 

### iv. Description des Erreurs <a name="errors"></a> 
## Codes d'erreur de l'API SoftwareAccessResource

| Code d'erreur                                                                   | Description                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <a name="usernotvalid"></a>`error.usernotvalid`                                 | L'identifiant de compte utilisateur fourni n'existe pas.                                                                                                                                                                                  |
| <a name="nullauthorizationkey"></a>`error.nullauthorizationkey`                 | Le header 'authorization-key' requis pour cette demande n'est pas fourni.                                                                                                                                                                 |
| <a name="invalidrequest"></a>`error.ventilationReportExtended.invalidrequest`   | Le corps de la requête est vide ou il manque la structure de données de base attendue dans la requête. Veuillez vérifier le schéma de l'objet VentilationControlData.                                                                     |
| <a name="validation"></a>`error.validation`                                     | Le résultat de contrôle ne respecte pas les règles de validation. Les erreurs de validation pour les champs en infraction sont retournées.                                                                                                |
| <a name="importForbidden"></a>`error.ventilationReportExtended.importForbidden` | Le contrôle est déjà publié sur l'Observatoire National Ventilation (soit par le propriétaire du rapport, soit par un autre utilisateur).                                                                                                 |
| <a name="updateForbidden"></a>`error.ventilationReportExtended.updateForbidden` | Le contrôle publié n'a pas été reconnu sur l'Observatoire National Ventilation. Il s'agit soit d'un nouveau contrôle, soit les identifiants indiqués sont erronés dans referenceDuRapport, IdentifiantDuBatiment ou IdentifiantDuSysteme. |
| <a name="importFailed"></a>`error.ventilationReportExtended.importFailed`       | Une exception inattendue s'est produite. Veuillez contacter le support pour résoudre le problème en indiquant la référence du rapport utilisé pour la requête.                                                                            |
| <a name="invalidId"></a>`error.invalidId`                                       | L'identifiant fourni dans l'URL de la requête n'existe pas dans l'Observatoire National Ventilation.                                                                                                                                      |

### Notes complémentaires

- **Code HTTP 401 (Unauthorized)** : Peut indiquer soit un échec de BasicAuth (nom de logiciel ou clé secrète invalides), soit que l'utilisateur n'a pas donné accès au logiciel à son compte.
- **Code HTTP 400 (Bad Request)** : Retourné pour les erreurs de validation ou les problèmes liés aux données fournies.
- **Code HTTP 403 (Forbidden)** : Retourné lorsque l'ID fourni dans l'URL n'existe pas.