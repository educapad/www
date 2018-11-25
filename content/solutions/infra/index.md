---
title: "Infrastructure"
date: 2018-11-25T17:41:08+01:00
---

Une infrastructure informatique robuste est la condition préalable à la réussite d'un projet de cartable numérique.

Les tablettes et la gestion de masse sont les points les plus simples de ce genre de projet bien qu'ils concentrent habituellement toute l'attention au détriment de l'infrastructure.

Il est vital de disposer d'une architecture fondamentalement orientée vers la performance, la sécurité et la montée en charge.

## Réseau filaire

Le réseau de l'école est un fondement des plus sensible, il doit être conçu pour garantir la sécurité des élèves et l'isolation des flux (un élève n'a pas à pouvoir joindre les serveurs administratifs).

Cela se traduit pour nous par une combinaison de switch Cisco Small Business SG350 en switch d'accès ainsi qu'au moins deux SG550 mis en « stack » pour servir de cœur de réseau de niveau 3 (inter-VLAN).

Les VLAN seront utilisé pour définir plusieurs classes d'équipement (Serveurs communs, serveurs administratifs, client administratif, client pédagogique, gestion des équipements, réseau IT, etc.) tout en prenant en compte la géographie des lieux.

Ainsi, une école disposant de plusieurs bâtiments aura plusieurs VLANs pédagogiques répondant tous aux mêmes critères de sécurité, mais regroupant les équipements géographiquement proches afin d'optimiser les flux et leur diffusion.

## Réseau WiFi

Concernant le WiFi, il est opportun de travailler avec les produits de [Aerohive](https://www.aerohive.com/products/access-points/). 

Ces produits nécessitent un abonnement pour fonctionner, mais représentent aujourd'hui l'état de l'art en termes d'architecture et d'optimisation des réseaux WiFi.

Il est normalement recommandé de faire une étude des lieux pour définir le nombre et l'emplacement optimal des points d'accès WiFi.

Toujours au vu de notre expérience, le nombre d'élèves par classe, les usages, et l'impératif de fonctionnement font qu'il y a au moins un point d'accès WiFi par salle de classe normale, plusieurs dans les amphis et les gymnases et éventuellement certaines à l'extérieur.

Si le WiFi ne fonctionne pas, il n'y a plus de cours, et les usages pédagogiques impliquent souvent du multimédia. L'iPad devenant l'outil principal de cours et permettant l'accès aux livres, il est totalement exclu que le réseau ne soit pas accessible.

## Accès Internet

L'accès à Internet doit se faire en très haut débit. Il est impératif de comprendre que lors que vous avez des centaines ou des milliers d'utilisateurs nécessitant Internet pour travailler sur leurs documents ou leurs livres, Internet doit fonctionner pleinement.

Cela passe obligatoirement par des abonnements en fibre optique de 100 Mb/s ou plus.

Concernant le filtrage de l'accès Internet, il est important de comprendre que les établissements scolaires sont confrontés à deux lois distinctes :

- l'obligation de protéger les élèves des contenus illégaux et pornographiques ;
- l'obligation de pouvoir identifier l'auteur d'un accès à un site Internet pour un jour et une heure donnée faite à tout organisme publiant un accès Internet.

Ces deux obligations ne sont pas liées, et n'excluent pas le respect du RGPD.

La solution efficace et légale que nous recommandons est la suivante.

Le filtrage de l'accès Internet se fait via un Cisco FirePOWER disposant des abonnements adéquats sans aucune authentification des utilisateurs. Le filtrage se base sur deux classes de machine : visible et invisible aux élèves.

Ainsi, les iPad des élèves, des enseignants, des documentalistes et de toute personne amenés à présenter quelque chose devant les élèves disposent des mêmes restrictions d'accès.

Les iPad et du BVS, de l'administration, de la direction disposent quant à un d'un accès éventuellement plus étendu.

Le filtrage basé sur Cisco FirePOWER permet un filtrage par réputation des URL auprès de [BrightCloud](https://www.brightcloud.com), un système mondialement utilisé est bien plus à jour que la « liste de Toulouse » et permettant une expérience utilisateur plus efficace que la plupart des solutions françaises habituellement recommandées.

Vous reposez avec ce système sur Cisco et BrightCloud pour filtrer les sites réputés terroristes, pornographiques, illégaux, ainsi que les proxys, VPN, site de jeux, sans pour autant bloquer automatiquement tout nouveau site existant sur Internet.

## Serveurs

Chaque site géographique de l'école (ou du groupe d'école) nécessitera un certain nombre de serveurs (Active Directory, gestion des caméras, applications Windows à distance pour les iPad, etc.). Pour héberger ces serveurs, il est aujourd'hui impératif de disposer d'un environnement de virtualisation.

Notre expérience montre que le système de virtualisation VMware vSphere en licence ROBO combiné à un service de sauvegarde Veeam répond particulièrement bien à l'ensemble des besoins d'une école.

En termes de serveurs physiques et d'espace de sauvegarde, un Dell VRTX avec un minimum de deux lames de calcul prend en charge l'ensemble des besoins standards et peut monter jusqu'à 4 lames pour les écoles les plus demandeuses.

Un NAS de sauvegarde Synology pour stocker les sauvegardes vient en complément du Dell.

Sans oublier de sauvegarder ces serveurs sur un autre site géographique (une autre école du groupe, un DataCenter, ou tout simplement chez OVH).

## Apple TV

L'Apple TV est un impératif pour chaque salle de cours. Elle permet de projeter le contenu d'un iPad au tableau.

Les Apple TV doivent être géré par Workspace ONE au même titre qu'un iPad, et doivent être attaché au réseau via un câble réseau et non par WiFi.

La connectivité WiFi de l'Apple TV est à réserver pour un usage domestique. L'usage en milieu professionnel et éducatif impose un fonctionnement filaire afin de réduire la consommation du WiFi déjà suffisamment occupé.