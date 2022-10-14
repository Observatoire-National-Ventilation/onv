
<a name="top"></a>
# <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/logo-onv.png?raw=true" align="left" height="80" width="200" > Observatoire National Ventilation <br>Guide d'utilisation pour l'accès opérateur

1. [Création et activation de votre compte](#creation)
2. [Modifier votre profil](#profilePage)
3. [Publier un résultat de contrôle](#publish)
    1. [Publication via l’outil de saisie manuelle](#import)
    2. [Publication via un logiciel du marché commercial](#byEditor)
4. [Consulter la liste de vos résultats de contrôle](#myReports)
5. [Mettre à jour un de vos résultats de contrôle](#updateReport)

----
 
## 1. Création et activation de votre compte <a name="creation"></a>

Votre compte sur l’Observatoire National Ventilation est créé par votre organisme de qualification, suite à l’obtention de votre qualification 8741. Vous êtes prévenu de la création de votre compte par un email intitulé “Activation de votre compte Observatoire National Ventilation” envoyé à l’adresse email que vous avez fournie à votre organisme de qualification.

Cet email contient un lien vous permettant d’activer votre compte et de [définir votre mot de passe](#setPassword). 

Si le lien ne vous permet pas d'accéder à la page d'initialisation du mot de passe, veuillez le copier-coller directement dans votre navigateur.

Attention, le lien d'activation reste valide 24 heures. Passé ce délai, vous devrez renouveler votre demande via la fonctionnalité "Mot de passe oublié".

<kbd>
    <a name="setPassword">
        <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/set_password.png?raw=true" alt="Créer votre mot de passe">
    </a>    
</kbd>    
<br/><br/>
 
Dans la page qui s’ouvre lorsque vous avez cliqué sur le lien, [choisissez votre mot de passe](#setPassword), de telle sorte à ce que l’indicateur de robustesse de celui-ci soit dans le vert pour une sécurité optimale de votre compte.

Vous êtes ensuite invité à vous connecter à votre compte avec:
 - votre numéro de dossier fourni par votre organisme de qualification, celui-ci est votre identifiant
 - et votre mot de passe.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/password_created_success.png?raw=true" alt="Succès de la configuration du mot de passe">
</kbd>
<br/><br/>

Vous êtes ensuite connecté à votre compte sur le site de l’Observatoire National Ventilation.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/logged-in_home.png?raw=true" alt="Page d'accueil après la connexion">
</kbd>
<br/><br/>

## 2. Modifier votre profil <a name="profilePage"></a>

En cliquant dans le menu du site sur “Compte” puis sur “Profil” vous accédez à [vos informations de profil](#pageProfile).

<kbd>
    <a name="pageProfile">
        <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/edit_profile.png?raw=true" alt="Page de profil">
    </a>
</kbd>
<br/><br/>
  
Vos informations de profil proviennent des informations dont dispose votre organisme de qualification. 

 - Les informations qui apparaissent sur fond gris (Nom, Prénom, Nom de Société, Siret, Département, Région) ne sont pas modifiables, hormis par l’organisme de qualification. 

 - Les informations qui apparaissent sur fond blanc (adresse email, téléphone, adresse) sont modifiables : n’hésitez pas à les mettre à jour si nécessaire, et notamment votre adresse email si vous en changez afin que vous puissiez toujours recevoir les informations venant de l’Observatoire National Ventilation. 

 - Cliquez sur le bouton “Sauvegarder” en bas de l’écran après avoir modifié une ou plusieurs de ces informations pour valider votre changement.

## 3. Publier un résultat de contrôle <a name="publish"></a>

La publication(alimentation de l’Observatoire National Ventilation) de vos résultats de contrôle de ventilation RE2020 est une obligation réglementaire. 

Pour chacun de vos contrôles de ventilation RE2020, vous devez alimenter l’Observatoire National Ventilation avec les données attendues par celui-ci.

Ces données seront utilisées à la fois pour le contrôle de votre activité par votre organisme de qualification et pour la construction d’indicateurs statistiques globaux des contrôles ventilation RE2020 réalisés sur le territoire national.

Il existe deux moyens de réaliser la publication: 
- par import via l’outil de saisie manuelle « RE2020_ONV_Outil_Saisie_Manuelle_V1.xlsx  » disponible dans l’onglet « Documentation » 

ou 

- par l’utilisation d’un logiciel du marché commercial conçu pour alimenter l’Observatoire National Ventilation.

### i. Publication via l’outil de saisie manuelle <a name="import"></a>

La publication de vos résultats de contrôles de ventilation est possible par l’intermédiaire d’un outil de saisie manuelle (fichier Excel) disponible gratuitement par téléchargement dans l’onglet « Documentation ». Ce fichier Excel est dénommé <a href="https://onv-test-1.eu-west-3.elasticbeanstalk.com/documentation" target="_blank">« RE2020_ONV_Outil_Saisie_Manuelle_V1.xlsx »</a>

Un mode d’emploi est intégré au fichier pour vous donner des indications sur la façon de le remplir.

Lorsque vous avez complété votre fichier avec les données de votre contrôle: 
- connectez vous sur le site de l’Observatoire National Ventilation
- et cliquez sur [“Mes contrôles de ventilation”](#myControls) dans le menu.


<kbd>
    <a name="myControls">
        <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/click_button_import.png?raw=true" alt="bouton d'importation du rapport de ventilation">
    </a>    
</kbd>
<br/><br/>

Cliquez sur le bouton “Importer un contrôle de ventilation” en haut à droite de votre écran.

Une fenêtre s’ouvre :

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/popup_import.jpg?raw=true" alt="Fenêtre popup d'importation">
</kbd>
<br/><br/>

Le bouton “Choisir un fichier” vous permet de sélectionner sur votre disque dur le fichier que vous souhaitez importer. Une fois celui-ci sélectionné, cliquez sur le bouton “Importer”.

Si le contenu du fichier respecte les règles attendues par l’Observatoire National Ventilation, alors le contrôle est publié et vous en avez la confirmation par ce message à l’écran :

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/import_success.png?raw=true" alt="Message de réussite de l'importation">
</kbd>
<br>

#### Message d’information/d’erreur/d’avertissement
A. Fichier non publié avec message d’information 

Si le contenu du fichier ne respecte pas une ou plusieurs des règles attendues par l’Observatoire National Ventilation liste dans le mode d’emploi l'outil de saisie manuelle), le contrôle n’est pas publié et un ou plusieurs messages vous informent des anomalies constatées. Vous êtes invité à corriger ces anomalies avant de pouvoir publier votre contrôle sur l’Observatoire National Ventilation. L’extraction ci-dessous est un exemple de messages d’anomalies.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/import_error.png?raw=true" alt="Message d'échec de l'importation">
</kbd>
<br/><br/>

B. Fichier non publié mais avec message d’erreur

Dans un cas particulier, votre contrôle s’importe correctement, mais un message d’avertissement vous est tout de même affiché : il s’agit du cas où l’ensemble des mesures fonctionnelles aux bouches normalement attendues pour le contrôle n’est pas présent dans votre fichier. Si l’absence de certaines de ces mesures fonctionnelles aux bouches n’est pas justifiée et qu’il s’agit d’un oubli ou d’une erreur, il vous faudra alors mettre à jour votre contrôle par la suite pour les ajouter.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/file_already_exists.png?raw=true" alt="Contrôle déjà existant">
</kbd>
<br/><br/>

C. Fichier publié mais avec message d’avertissement

Votre contrôle s’importe correctement, mais un message d’avertissement vous est tout de même affiché : il s’agit du cas où l’ensemble des mesures fonctionnelles aux bouches normalement attendues pour le contrôle n’est pas présent dans votre fichier. Si l’absence de certaines de ces mesures fonctionnelles aux bouches n’est pas justifiée et qu’il s’agit d’un oubli ou d’une erreur, il vous faudra alors mettre à jour votre contrôle par la suite pour les ajouter.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/import_with_warning.png?raw=true" alt="Importation réussie avec message d'avertissement">
</kbd>
<br/><br/>

### ii. Publication via un logiciel du marché commercial <a name="byEditor"></a>

La publication de vos résultats de contrôles de ventilation est aussi possible par l’intermédiaire d’un logiciel du marché disposant des fonctionnalités nécessaires pour communiquer avec l’Observatoire National Ventilation, 
 - Si vous disposez de ce type de logiciel référez-vous au mode d’emploi de celui-ci pour savoir comment réaliser vos publications sur l’Observatoire National Ventilation.

Nota: lors de votre première publication, le logiciel vous redirigera vers votre compte sur le site de l'Observatoire National Ventilation afin que vous donniez l'autorisation à votre logiciel de publier vos contrôles sur votre compte.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/grant-access.png?raw=true" alt="Accorder l'accès au logiciel">
</kbd>
<br/><br/>

## 4. Consulter la liste de vos résultats de contrôle <a name="myReports"></a>

Connectez-vous sur le site de l’Observatoire National Ventilation, et cliquez sur “Mes contrôles de ventilation” dans le menu.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/all_reports.png?raw=true" alt="Tous les rapports">
</kbd>
<br/><br/>

Vous visualisez ainsi la liste complète des contrôles de ventilation que vous avez publiés, avec les informations suivantes : 
 - la référence du rapport 
 - le nom de l’opération 
 - l’identifiant du bâtiment
 - le code postal de l'opération
 - la date de création du contrôle sur l’Observatoire National Ventilation
 - la conformité réglementaire du système de ventilation contrôlé
 - la date de vérification sur site du système de ventilation
 - et l’identifiant du système de ventilation
 
Pour chacun de vos contrôles, vous avez accès à droite à un bouton « Editer » qui vous permet de mettre à jour vos résultats de contrôle.

## 5. Mettre à jour un de vos résultats de contrôle <a name="updateReport"></a>

Pour mettre à jour un de vos résultats de contrôle, vous disposez d’un bouton « Editer » au bout de ligne d’un de vos contrôles dans la section “Mes contrôles de ventilation”.

En sélectionnant « Editer », une fenêtre s’ouvre vous invitant à sélectionner un fichier de contrôle, de la même façon que pour l’import d’un nouveau contrôle.

Lorsque vous avez sélectionné le fichier et validé l’import, l’Observatoire National Ventilation vérifie que la référence du rapport, l’identifiant du bâtiment et l’identifiant du système de ventilation correspondent bien à ceux du contrôle sélectionné. 

Si toutes les conditions sont respectées le contrôle existant est remplacé par le nouveau fichier. 

Dans le cas contraire, un message d’erreur apparaît, et vous invite:
- à sélectionner un fichier conforme 

ou

- à importer un nouveau contrôle si cela était votre intention.

<br/><br/>
<a href="#top"> <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/arrow_top.png?raw=true"  height="10" width="20" alt="Haut de page">HAUT DE PAGE</a>  
