---
title: "Fédération d'identité"
date: 2018-11-25T17:37:31+01:00
---

La fédération d'identité est le service assuré par Workspace ONE Access. Le principe est simple : un service tiers se repose sur un service sous votre contrôle pour identifier vos utilisateurs.

Par exemple, lorsque l'utilisateur cherche à accéder à ses e-mails ou ses documents Google Suite depuis son iPad, il doit être authentifié. S'il ne l'est pas déjà, Google redirigera l'utilisateur vers WS1 Access afin d'être authentifié. Si la tablette est gérée par l'école, WS1 Access découvrira automatiquement l'identité de l'utilisateur et reniera la réponse à Google. Si l'équipement n'est pas géré (comme pour un accès aux mails depuis un ordinateur personnel), WS1 Access pourra demander un identifiant et mot de passe, ou simplement refuser l'accès (en fonction de vos réglages) et renverra la réponse à Google.

Ainsi, vous pouvez permettre au personnel administratif d'utiliser Google Suite depuis des machines personnelles, mais pas les élèves. Et pour les iPad contrôlés par l'école, aucun besoin d'authentification.

Pour que cela fonctionne, WS1 Access doit être intégré avec votre Active Directory et votre gestionnaire de terminaux Workspace ONE UEM. Une preuve d'identité sera déposée par UEM sur le terminal permettant de déclencher une authentification Kerberos de l'iPad vers WS1 Access.

Ce mécanisme est compatible avec tout service en ligne supportant SAML ou OAuth (deux protocoles de déport d'authentification).

Ces protocoles sont très largement utilisés à travers Internet et le monde des éditeurs de logiciel en ligne. Cependant, il se peut que vous trouviez vos éditeurs de logiciel français en retard sur ce domaine. N'hésitez pas en tant que client à leur indiquer que leur manque de modernité vous coute du temps de support aux utilisateurs, et donc de l'argent.
