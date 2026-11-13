# Rattachement au moteur — contrat à concevoir

## Faits de départ
Le prototype loop.py fourni comme source possède init, ingest, classify, link, validate, status et export. La classification est fournie à la commande ; ses catégories décrivent la nature (REQUIREMENT, MODEL, PLAN, etc.). Il ne charge pas les identifiants BASE. link ne cible que des événements du journal existant.

Looping- est un dépôt distinct disposant du moteur de gouvernance de son template. Son intake doit être réutilisé et réconcilié avant toute extension. La présence des fichiers ne certifie pas le fonctionnement live de toutes ses portes : voir ADMISSION_AND_BASELINE.md.

## Contrat proposé
- Charger une projection identifiée de BASE : version, provenance, empreinte, nœuds et relations.
- Conserver la nature de l’information séparément du thème BASE, de l’état de décision et de l’avancement.
- Relier l’information à un projet explicitement identifié et aux propriétaires documentaires de ce projet.
- Préparer un profil indiquant les domaines de besoin à examiner, les conditions d’applicabilité et les informations manquantes.
- Conserver les propositions, contradictions et décisions avec leur justification.
- Examiner les dépendances affectées avant d’actualiser cahier des charges, architecture, plan et preuves.
- Sélectionner uniquement des travaux dont les prérequis et autorisations réelles sont satisfaits.
- Conserver une reprise et des limites d’exécution.

## Compatibilité
Les anciennes catégories et événements restent interprétables. Les relations BASE (mobilise, présente, associe...) conservent leur sens et ne sont pas transformées silencieusement en dépendances de code ou en relations d’événements.

La projection ne constitue pas une seconde autorité éditée indépendamment. La correspondance au modèle d’intake natif, à ses révisions et aux propriétaires reste à décider avant implémentation.

## Scénarios futurs de validation
Rattachement valide ; identifiant inconnu ; parent absent ; information hors champ ; ambiguïté ; contradiction ; remplacement explicite ; changement de version BASE ; reprise après interruption ; absence d’autorité ; conservation d’un ancien événement sans références BASE.
