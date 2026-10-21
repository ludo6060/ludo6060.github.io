# Wilo FireFighting — Assistant technicien V0.6

Application : https://ludo6060.github.io/sifire/

## Périmètre

SiFire, FireSet et procédures transversales de la formation Bari, en français, néerlandais, anglais et allemand : pré-mise en service, mise en service, maintenance, diagnostics, alignement, calculs, outillage et rapports. Les références et informations manquantes sont indiquées dans l’application. Version de travail à valider avant usage prescriptif ; aucune certification automatique de conformité.

## Module FPT / Bimotor

La référence Clarke est retirée. Le module additionne les pertes documentées : longueur droite × perte linéique, coudes, flexible, silencieux et autres accessoires. Il compare le total à la contre-pression maximale documentée du moteur exact.

Le calcul exige la référence moteur complète, les sources de la limite et des pertes, le débit réel des gaz, la température, les conditions de fonctionnement et la confirmation que les coefficients correspondent à ces conditions. Une valeur absente reste inconnue ; zéro doit être saisi explicitement. Un changement de conditions invalide la confirmation.

Ce module n’est pas un calculateur officiel FPT ou Bimotor. Les catalogues liés fournissent des exemples d’identification, pas des coefficients de pertes. Il ne sélectionne pas automatiquement de diamètre, ne convertit pas les débits normalisés en débits chauds et ne traite pas une ligne à diamètres multiples. Les abaques constructeur manquants restent nécessaires. Une mesure réelle de contre-pression doit vérifier le résultat.

## Données et accès

L’application et ses références sont publiques sur GitHub Pages. Les visiteurs n’obtiennent aucun droit de modification du dépôt. Les données personnelles d’intervention et les sauvegardes JSON sont chiffrées localement par mot de passe (AES-256-GCM, PBKDF2-HMAC-SHA256) ; elles ne sont pas synchronisées entre appareils. Verrouillage après cinq minutes d’inactivité. Aucun mécanisme de récupération du mot de passe. Les rapports imprimés ou exportés en PDF sont lisibles et doivent être protégés séparément.

## Vérification V0.6

Tests réussis : vues et traductions, calcul des pertes, dépassement de limite, données manquantes, invalidation après changement, restauration des résultats et chiffrement réel (mot de passe incorrect, altération, sauvegardes).
