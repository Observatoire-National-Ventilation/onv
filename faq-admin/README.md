#   <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/logo-onv.png?raw=true" align="left" height="80" width="200" > Observatoire National Ventilation - FAQ Administrateurs

## FAQ à destination des administrateurs de l'Observatoire National Ventilation.

* [2022-1 Que faire si un utilisateur a perdu le mail d'activation de son compte?](#faq2022-1)
* [2022-2 Que faire si un éditeur de logiciel n'a plus accès a sa clé de sécurité](#faq2022-2)

## 2022-1 Que faire si un utilisateur a perdu le mail d'activation de son compte? <a name="faq2022-1"></a>

Il est possible de demander l'envoi d'un nouveau mail d'activation pour un compte qui n'a pas encore été activé depuis l'interface d'administration de l'Observatoire.

Cette opération nécessite un accès Administrateur à la plateforme.

Se rendre dans le menu Administration > Gestion des utilisateurs puis cliquer sur le bouton "Ré-envoyer le mail d'activation" au niveau du compte concerné.

<kbd>
    <img src="https://github.com/dooApp/onv/blob/docs/wiki-images/admin_resend_email.png?raw=true" alt="Renvoyer l'email du mot de passe">
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

L'éditeur peut alors suivre [la procédure initiale](https://dooapp.github.io/onv/access-editor/#2-api-reference-) pour obtenir une nouvelle clé de sécurité.
