# Impression d'étiquettes & codes-barres (Xprinter / TSPL)

Deux applications Flutter Desktop (Windows) pour l'étiquetage des produits sur imprimantes thermiques Xprinter.

> Projet réalisé par **Fayçal Gheroufella** chez SINAL (distribution optique, Algérie). Le code source appartient à l'entreprise et reste privé ; démonstration possible en entretien.

## Fonctionnalités

- **Étiquettes produit 60×40 mm** : marquage CE, marque/modèle, IMEI et numéro de série en **Code128**
- Dessin de l'étiquette en image 1-bit à **203 dpi** (480×320 points), puis génération de commandes **TSPL** brutes (`SIZE`, `GAP`, `DENSITY`, `SPEED`, `BITMAP`)
- Envoi direct au spouleur Windows via `winspool.dll` (`OpenPrinter` / `WritePrinter`) avec **dart:ffi**, sans passer par le pilote graphique
- Orientation paysage / portrait, rotation 180°, mode test vers fichier, aperçu PNG, tests unitaires
- **Codes-barres en série** : plage de codes (début → fin, quantité) ou import Excel, format configurable (40×20 mm par défaut), aperçu PDF, barre de progression, imprimante mémorisée

## Technologies

Flutter Desktop (Windows) · Dart · dart:ffi · barcode · pdf / printing · window_manager · shared_preferences

## En chiffres

~1 100 lignes (étiquettes) + ~1 900 lignes (codes-barres en série)  
Mai – oct. 2026.

## Organisation du projet

- `etiquette/` — étiquettes produit CE / IMEI / n° de série en TSPL
- `barcode-range/` — impression en série de codes-barres Code128

## Contact

gheroufellafaycal@gmail.com · [LinkedIn](https://linkedin.com/in/faysal-gheroufella-4a7969355)
