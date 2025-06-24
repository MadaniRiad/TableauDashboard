# 🚧 Analyse des Accidents de la Route en France - Projet Tableau

Ce projet a été réalisé dans le cadre d'une étude sur l'accidentologie en France à l'aide de **Tableau Prep Builder** pour le traitement de données et **Tableau Desktop** pour la visualisation.

## 🎯 Objectifs du projet

- Nettoyer et regrouper des jeux de données d’accidents de la route (issus de plusieurs années).
- Intégrer les données des radars fixes (pas de clé commune) via une jointure sur les noms de route.
- Étudier l’évolution des accidents en lien avec l’implantation des radars.
- Créer un dashboard de **validation** pour vérifier la cohérence des données préparées.

---

## 🧰 Outils utilisés

- **Tableau Prep Builder** : pour l’union, le nettoyage, la jointure conditionnelle des jeux de données.
- **Tableau Desktop** : pour la création des dashboards et visualisations interactives.

---

## 🧼 Préparation des données (Tableau Prep)

- **Jeux de données d’accidents** fusionnés par année.
- Suppression des enregistrements avec des champs critiques nuls.
- Normalisation des noms de routes pour permettre la jointure avec les données radars :
  - Suppression des espaces parasites.
  - Nettoyage des commentaires et anomalies.
- Jointure avec les données radars :
  - Sur le **nom de la route** pour les nationales/autoroutes.
  - Sur **nom de la route + département** pour les routes départementales.

📂 **Extrait du flow Prep** :
![Flow Tableau Prep](./MADANI-Riad.tflx)

---

## 📊 Visualisations réalisées (Tableau)

### 🔎 Validation du jeu de données

- Nombre d'accidents par type de route
- Répartition géographique (ex. Pyrénées-Atlantiques)
- Évolution des accidents par type de voie et année
- Lien entre implantation des radars fixes et diminution des accidents

📈 **Exemple : Répartition des accidents par type de route**
![Type de route](./MADANI-Riad.twb)

📍 **Zoom sur le département 64 (Pyrénées-Atlantiques)**
![PA Accidents](./MADANI-Riad.twb)

📉 **Évolution temporelle**
![Évolution](./MADANI-Riad.twb)

---

## 🧪 Dashboard de validation

Le dashboard "Validation" regroupe toutes les vérifications effectuées sur les données :

- Problèmes détectés : doublons, incohérences sur les libellés, valeurs manquantes.
- Solutions appliquées dans Tableau Prep (ex. filtre, reformatage).
- Résultats validés avec des KPIs clairs et visuels.

🖼️ **Aperçu du dashboard de validation**
![Dashboard Validation](./MADANI-Riad.twb)

---

## 📁 Arborescence du projet
/tableau-accidents-route
├── BDD AccidentsRadars.hyper
├── Accidents_Tableau.twb (MADANI-Riad.twb)
├── PrepFlow_Accidents.tfl (MADANI-Riad.tflx)
└── README.md
