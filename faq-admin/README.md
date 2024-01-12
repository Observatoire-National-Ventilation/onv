## ONV - Guide accès Administrateurs

#   <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/logo-onv.png?raw=true" align="left" height="80" width="200" > Observatoire National Ventilation - FAQ Administrateurs

## FAQ à destination des administrateurs de l'Observatoire National Ventilation.

* [2022-1 Que faire si un utilisateur a perdu le mail d'activation de son compte?](#faq2022-1)
* [2022-2 Que faire si un éditeur de logiciel n'a plus accès a sa clé de sécurité](#faq2022-2)
* [2022-3 Comment créer un nouveau compte utilisateur?](#faq2022-3)

## 2022-1 Que faire si un utilisateur a perdu le mail d'activation de son compte? <a name="faq2022-1"></a>

Il est possible de demander l'envoi d'un nouveau mail d'activation pour un compte qui n'a pas encore été activé depuis l'interface d'administration de l'Observatoire.

Cette opération nécessite un accès Administrateur à la plateforme.

Se rendre dans le menu Administration > Gestion des utilisateurs puis cliquer sur le bouton "Ré-envoyer le mail d'activation" au niveau du compte concerné.

<kbd>
    <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/admin_resend_email.png?raw=true" alt="Renvoyer l'email du mot de passe">
</kbd>
<br/><br/>

## 2022-2 Que faire si un éditeur de logiciel n'a plus accès a sa clé de sécurité <a name="faq2022-2"></a>

Il n'est pas possible de récupérer la clé de sécurité d'un éditeur depuis l'Observatoire. Si un éditeur a perdu sa clé de sécurité, il est nécessaire de supprimer la clé actuelle et d'en créer une nouvelle.

Pour ce faire, l’éditeur devra faire une demande officielle à l’administrateur (Mail, courrier) afin de demander une nouvelle clé de sécurité.
En retour, l’administrateur lui communiquera par mail ou courrier la date pour lui permettre de créer sa nouvelle clé de sécurité. 

**Attention** : en suivant cette procédure, la clé actuelle de sécurité de l'éditeur sera supprimée et son logiciel ne pourra plus communiquer avec l'Observatoire National Ventilation avec cette clé.

Cette opération peut-être effectuée par un administrateur de la plateforme :

* se rendre dans le menu Entités > Software
* cliquer sur le bouton "Editer" du logiciel concerné
* effacer la clé de sécurité dans le formulaire d'édition et enregistrer

L'éditeur peut alors suivre [la procédure initiale](https://github.com/Observatoire-National-Ventilation/onv/access-editor/#2-api-reference-) pour obtenir une nouvelle clé de sécurité.

## 2022-3 Comment créer un nouveau compte utilisateur? <a name="faq2022-3"></a>

Pour créer des comptes opérateurs, la fonctionnalité d'import d'une liste d'opérateurs par fichier Excel est la méthode à privilégier car la plus simple et la plus rapide.<br/>

Pour créer un compte éditeur de logiciel, un formulaire spécifique existe publiquement et permet à l'éditeur de se créer son propre compte.<br/>

Pour les comptes administration (DHUP, CEREMA...), membres d'un organisme de qualification, ou nouvel administrateur technique de l'ONV, c'est avec le rôle d'administrateur ROLE-ADMIN que vous pouvez procéder pour créer le compte.<br/>

Pour cela, suivez les étapes suivantes :
* Rendez-vous dans la rubrique "Administration">"Gestion des utilisateurs"
* Cliquez sur le bouton "Créer un nouvel utilisateur"
* Renseignez le login, le nom, prénom et email de l'utilisateur
* Sélectionnez le ou les rôles de l'utilisateur. Il est possible de lui en attribuer plusieurs en maintenant la touche "Ctrl" enfoncée, afin qu'il ait accès aux fonctionnalités de plusieurs rôles différents à la fois.
* Cliquez sur le bouton "Sauvegarder" en bas de la page. Un email est envoyé automatiquement à l'adresse indiquée, invitant l'utilisateur à se choisir un mot de passe pour activer son compte et l'utiliser.
* Retournez dans la rubrique "Administration">"Gestion des utilisateurs"
* Retrouvez tout à la fin de la liste des utilisateurs le nouveau compte que vous venez de créer, et notez son "ID" tout à gauche de la ligne.
* Rendez-vous dans la rubrique "Entités">"User Profile"
* Cliquez sur le bouton "Créer un nouveau User Profile"
* Renseignez les informations "Téléphone", "Nom de Société", "Siret", "Adresse", "Département", "Région"
* Renseignez dans le champ "User" l'ID du compte utilisateur que vous venez de créer
* Si il s'agit d'un compte opérateur ou d'un membre d'un organisme de qualification, renseignez dans le champ "Qualification Body" le "Name" de l'organisme auprès duquel il est certificé, ou auquel il appartient.
* Cliquez sur le bouton "Sauvegarder"
* La création du compte est achevée.

<br/><br/>
<a href="#top"> <img src="https://github.com/Observatoire-National-Ventilation/onv/blob/docs/wiki-images/arrow_top.png?raw=true"  height="10" width="20" alt="Haut de page">HAUT DE PAGE</a>  
