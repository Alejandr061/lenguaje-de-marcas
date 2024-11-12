# Model del Projecte Rainbow Six

Aquest projecte representa l'estructura dels operadors i mapes del joc **Rainbow Six**, un joc de trets tàctic on cada operador té habilitats i rols específics dins d'un escenari de combat. Aquesta estructura XML facilita la definició dels operadors i els mapes amb la informació essencial per gestionar el joc.

## Elements Principals

### RAINBOW-SIX
L'element arrel que inclou els elements principals:
- **operadors**: La llista de tots els operadors disponibles.
- **mapes**: La llista de mapes o escenaris on es desenvolupa el joc.

### operadors
Agrupa diversos **operador**, cadascun amb atributs i elements per a la seva identificació i equipament.

### operador
Defineix un operador individual amb:
- **Atributs**: 
  - `id` (tipus `ID`), identificador únic de cada operador.
  - `rol`, que pot ser "atacant" o "defensor".
- **Elements**:
  - **nom**: El nom de l'operador.
  - **funcio**: Rol específic dins de l'equip.
  - **armes**: Tipus d'armes disponibles.
  - **habilitats**: Capacitats especials de l'operador.

### armes
Conté una col·lecció de diferents tipus d'armes, com **pistola**, **escopeta**, **subfusil**, entre d'altres. Cada arma pot referenciar un operador amb `operador_id` de tipus `IDREF` per associar l'arma al seu usuari.

### habilitats
Defineix les habilitats especials, que poden ser de tipus **habilitat_atacant** o **habilitat_defensor**, segons el rol de l'operador.

### mapes
Agrupa diversos **mapa**, cada un representa un escenari de joc.

### mapa
Inclou informació sobre un escenari de joc amb els següents elements:
- **nom**: Nom del mapa.
- **foto**: Enllaç a la imatge.
- **informacio**: Descripció general.
- **historia_real**: Origen o inspiració real, opcional.

## Resum de Relacions amb ID i IDREF
- **operador** defineix un `id` únic (de tipus `ID`), utilitzat per les armes a través de l'atribut `operador_id` (`IDREF`) per establir una connexió directa entre l'operador i les seves armes.
