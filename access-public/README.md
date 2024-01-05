
<a name="top"></a>
# <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/logo-onv.png?raw=true" align="left" height="80" width="200" > Observatoire National Ventilation <br>Guide d'utilisation pour l'accès public

1. [Page d'Accueil](#home)
2. [Page Statistiques](#statistics)
    1. [Statistique 1](#stat1)
    2. [Statistique 2](#stat2)
3. [Pages Liens Utiles](#usefulLinks)

----
  
## 1. Page d'Accueil <a name="home"></a>

Votre compte sur l’Observatoire National Ventilation est créé par votre organisme de qualification, suite à l’obtention de votre qualification 8741. Vous êtes prévenu de la création de votre compte par un email intitulé “Activation de votre compte Observatoire National Ventilation” envoyé à l’adresse email que vous avez fournie à votre organisme de qualification.

Cet email contient un lien vous permettant d’activer votre compte et de [définir votre mot de passe](#setPassword). 

Si le lien ne vous permet pas d'accéder à la page d'initialisation du mot de passe, veuillez le copier-coller directement dans votre navigateur.

Attention, le lien d'activation reste valide 24 heures. Passé ce délai, vous devrez renouveler votre demande via la fonctionnalité "Mot de passe oublié".

<kbd>
    <a name="setPassword">
        <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/set_password.png?raw=true" alt="Créer votre mot de passe">
    </a>    
</kbd>    
<br/><br/>
 
Dans la page qui s’ouvre lorsque vous avez cliqué sur le lien, [choisissez votre mot de passe](#setPassword), de telle sorte à ce que l’indicateur de robustesse de celui-ci soit dans le vert pour une sécurité optimale de votre compte.

Vous êtes ensuite invité à vous connecter à votre compte avec:
 - votre numéro de dossier fourni par votre organisme de qualification, celui-ci est votre identifiant
 - et votre mot de passe.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/password_created_success.png?raw=true" alt="Succès de la configuration du mot de passe">
</kbd>
<br/><br/>

Vous êtes ensuite connecté à votre compte sur le site de l’Observatoire National Ventilation.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/logged-in_home.png?raw=true" alt="Page d'accueil après la connexion">
</kbd>
<br/><br/>

## 2. Page statistiques <a name="statistics"></a>

La publication(alimentation de l’Observatoire National Ventilation) de vos résultats de contrôle de ventilation RE2020 est une obligation réglementaire. 

Pour chacun de vos contrôles de ventilation RE2020, vous devez alimenter l’Observatoire National Ventilation avec les données attendues par celui-ci.

Ces données seront utilisées à la fois pour le contrôle de votre activité par votre organisme de qualification et pour la construction d’indicateurs statistiques globaux des contrôles ventilation RE2020 réalisés sur le territoire national.

Il existe deux moyens de réaliser la publication: 
- par import via l’outil de saisie manuelle « RE2020_ONV_Outil_Saisie_Manuelle_V1.xlsx  » disponible dans l’onglet « Documentation » 

ou 

- par l’utilisation d’un logiciel du marché commercial conçu pour alimenter l’Observatoire National Ventilation.

### i. Publication via l’outil de saisie manuelle <a name="stat1"></a>

La publication de vos résultats de contrôles de ventilation est possible par l’intermédiaire d’un outil de saisie manuelle (fichier Excel) disponible gratuitement par téléchargement dans l’onglet « Documentation ». Ce fichier Excel est dénommé <a href="https://onv-test-1.eu-west-3.elasticbeanstalk.com/documentation" target="_blank">« RE2020_ONV_Outil_Saisie_Manuelle_V1.xlsx »</a>

Un mode d’emploi est intégré au fichier pour vous donner des indications sur la façon de le remplir.

Lorsque vous avez complété votre fichier avec les données de votre contrôle: 
- connectez vous sur le site de l’Observatoire National Ventilation
- et cliquez sur [“Mes contrôles de ventilation”](#myControls) dans le menu.


<kbd>
    <a name="myControls">
        <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/click_button_import.png?raw=true" alt="bouton d'importation du rapport de ventilation">
    </a>    
</kbd>
<br/><br/>

Cliquez sur le bouton “Importer un contrôle de ventilation” en haut à droite de votre écran.

Une fenêtre s’ouvre :

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/popup_import.jpg?raw=true" alt="Fenêtre popup d'importation">
</kbd>
<br/><br/>

Le bouton “Choisir un fichier” vous permet de sélectionner sur votre disque dur le fichier que vous souhaitez importer. Une fois celui-ci sélectionné, cliquez sur le bouton “Importer”.

Si le contenu du fichier respecte les règles attendues par l’Observatoire National Ventilation, alors le contrôle est publié et vous en avez la confirmation par ce message à l’écran :

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/import_success.png?raw=true" alt="Message de réussite de l'importation">
</kbd>
<br>

#### Message d’information/d’erreur/d’avertissement
A. Fichier non publié avec message d’information 

Si le contenu du fichier ne respecte pas une ou plusieurs des règles attendues par l’Observatoire National Ventilation liste dans le mode d’emploi l'outil de saisie manuelle), le contrôle n’est pas publié et un ou plusieurs messages vous informent des anomalies constatées. Vous êtes invité à corriger ces anomalies avant de pouvoir publier votre contrôle sur l’Observatoire National Ventilation. L’extraction ci-dessous est un exemple de messages d’anomalies.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/import_error.png?raw=true" alt="Message d'échec de l'importation">
</kbd>
<br/><br/>

B. Fichier non publié mais avec message d’erreur

Dans un cas particulier, votre contrôle s’importe correctement, mais un message d’avertissement vous est tout de même affiché : il s’agit du cas où l’ensemble des mesures fonctionnelles aux bouches normalement attendues pour le contrôle n’est pas présent dans votre fichier. Si l’absence de certaines de ces mesures fonctionnelles aux bouches n’est pas justifiée et qu’il s’agit d’un oubli ou d’une erreur, il vous faudra alors mettre à jour votre contrôle par la suite pour les ajouter.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/file_already_exists.png?raw=true" alt="Contrôle déjà existant">
</kbd>
<br/><br/>

C. Fichier publié mais avec message d’avertissement

Votre contrôle s’importe correctement, mais un message d’avertissement vous est tout de même affiché : il s’agit du cas où l’ensemble des mesures fonctionnelles aux bouches normalement attendues pour le contrôle n’est pas présent dans votre fichier. Si l’absence de certaines de ces mesures fonctionnelles aux bouches n’est pas justifiée et qu’il s’agit d’un oubli ou d’une erreur, il vous faudra alors mettre à jour votre contrôle par la suite pour les ajouter.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/import_with_warning.png?raw=true" alt="Importation réussie avec message d'avertissement">
</kbd>
<br/><br/>

### ii. Publication via un logiciel du marché commercial <a name="stat2"></a>

La publication de vos résultats de contrôles de ventilation est aussi possible par l’intermédiaire d’un logiciel du marché disposant des fonctionnalités nécessaires pour communiquer avec l’Observatoire National Ventilation, 
 - Si vous disposez de ce type de logiciel référez-vous au mode d’emploi de celui-ci pour savoir comment réaliser vos publications sur l’Observatoire National Ventilation.

Nota: lors de votre première publication, le logiciel vous redirigera vers votre compte sur le site de l'Observatoire National Ventilation afin que vous donniez l'autorisation à votre logiciel de publier vos contrôles sur votre compte.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/grant-access.png?raw=true" alt="Accorder l'accès au logiciel">
</kbd>
<br/><br/>

## 3. Page Liens Utiles <a name="usefulLinks"></a>

<br/><br/>
<a href="#top"> <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/arrow_top.png?raw=true"  height="10" width="20" alt="Haut de page">HAUT DE PAGE</a>  

