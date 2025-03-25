# Projet Tensions sur le Marché du Travail - Unédic

Ce projet vise à développer une carte interactive au niveau des zones d'emploi affichant un indicateur de tension sur le marché du travail. La carte permet d’identifier des catégories de territoires en fonction de l’intensité de la tension sur une catégorie professionnelle donnée, facilitant ainsi l’analyse statistique et éclairant les décisions en matière de politiques publiques.

## **Contexte du projet**

Le projet résulte d’une collaboration entre le MSc&T « Data and Economics for Public Policy » (École Polytechnique, ENSAE & Télécom Paris) et l'Unédic (association chargée par délégation de service public de la gestion de l'assurance chômage en France). Il a été développé dans le cadre d’un défi proposé aux étudiants, visant la création d’un outil d’observation et d’analyse des dynamiques du marché du travail à une échelle territoriale fine.

## **La Carte Interactive**

### Fonctionnalités

L'application permet de visualiser la tension sur le marché du travail en France en 2020 (les données plus récentes n'étant pas disponibles à l'échelle du projet) à travers une carte interactive et des graphiques dynamiques. Les utilisateurs peuvent filtrer les données par catégorie d'emploi, type de demandeur d'emploi et région, et explorer l'évolution mensuelle des indicateurs. L'outil fournit une analyse en temps réel de la situation du marché du travail à différents niveaux géographiques.

### **Sources de données**

Le projet s’appuie sur des données administratives et des données en libre accès :
- **Jocas 2020 (Dares)** : Disponible via l’ADISP ou en lien direct avec la Dares pour des millésimes plus récents.
- **France Travail Open Data** : Données trimestrielles diffusées sur les demandeurs d’emploi au niveau communal pour les communes de plus de 5 000 habitants, avec des ventilations par métier, qualification, diplôme, sexe et âge.

### **Applications Potentielles**

-   **Analyse exploratoire des déséquilibres du marché du travail** à différentes échelles géographiques.
-   **Identification de clusters de territoires** selon l’offre et la demande d’emploi.
-   **Recommandations de politiques publiques** pour remédier aux inadéquations entre les offres et les demandeurs d’emploi.

## **Exécution de l’Application**

L’outil est accessible en exécutant le script "labour_tightness_dashboard.ipynb" situé dans `./app`. Tous les fichiers nécessaires se trouvent dans le dossier `./data`.

Pour les utilisateurs souhaitant reproduire le projet depuis le début, les scripts nécessaires sont fournis dans le répertoire `./src`, avec des consignes détaillées dans les fichiers README. Certains ensembles de données de grande taille (JOCAS) doivent être téléchargés manuellement.

## **Structure des Fichiers**
```
├── README.md                                      <- Documentation principale du projet
├── LICENSE                                        <- Licence du projet
├── app                                            <- Scripts pour exécuter l’outil de cartographie interactive
├── data                                           <- Toutes les données
│   ├── 1- Raw Data                                <- Données brutes
│   ├── 2- Formatted Data                          <- Données formatées
│   ├── 3- Final Data                              <- Données finales
│   ├── linking tables                             <- Tables de liaison
│   └── shapefiles                                 <- Shapefiles nécessaires à la cartographie
├── src                                            <- Code source pour le traitement et l’analyse des données.
│   ├── 00_explore_jocas_missing_values.ipynb      <- Exploration des valeurs manquantes de JOCAS
│   ├── 01_match_communes_with_shapefile.ipynb     <- Correspondance des communes avec le shapefile
│   ├── 02_clean_rome_fap_mapping.ipynb            <- Nettoyage de la table de correspondance ROME-FAP
│   ├── 03_process_stmt_demand.ipynb               <- Traitement des données STMT (demande)
│   ├── 04_process_jocas_supply.ipynb              <- Traitement des données JOCAS (offre)
│   └── 05_compute_labour_tightness_ratio.ipynb    <- Calcul du ratio de tension sur le marché du travail
├── docs                                           <- Références et documents utilisés lors du projet
├── reports                                        <- Note méthodologique + diaporama de présentation
```


## **Contributions & Contact**

Pour toute suggestion ou pour signaler des erreurs, vous pouvez contacter :

-   Alfonso Awadalla-Carreño : [alfonso.awadalla-carreno@polytechnique.edu](mailto:alfonso.awadalla-carreno@polytechnique.edu)
-   Cynthia Francis : [cynthia.francis@polytechnique.edu](mailto:cynthia.francis@polytechnique.edu)
-   Anahi Reyes-Miguel : [anahi.reyes-miguel@polytechnique.edu](mailto:anahi.reyes-miguel@polytechnique.edu)

Les contributions et collaborations visant à améliorer l’outil sont les bienvenues.

------------------------------------------------------------------------

# Labour Market Tightness Project - Unédic

This project aims to develop an interactive map at the employment zone level displaying a labour market tightness indicator. The map allows the identification of territorial categories based on the intensity of tightness in a given job category, facilitating statistical analysis and informing public policy decisions.

## **Project Context**

The project is the result of a collaboration between the MSc&T "Data and Economics for Public Policy" (École Polytechnique, ENSAE & Télécom Paris) and Unédic (the association in charge of managing unemployment insurance in France by public service delegation). It was developed as part of a student challenge aimed at creating a tool for observing and analyzing labour market dynamics at a fine territorial scale.

## **Interactive Map**

### Features

The application allows users to visualize labour market tightness in France for 2020 (more recent data is unavailable for this project scale) through an interactive map and dynamic graphs. Users can filter data by job category, jobseeker type, and region, and explore the monthly evolution of indicators. The tool provides real-time analysis of the labour market situation at various geographical levels.

### **Data Sources**

The project relies on administrative and publicly available data:
- **Jocas 2020 (Dares)**: Available via ADISP or directly from Dares for more recent datasets.
- **France Travail Open Data**: Quarterly data on jobseekers at the commune level for communes with more than 5,000 inhabitants, with breakdowns by job, qualification, diploma, gender, and age.

### **Potential Applications**

-   **Exploratory analysis of labour market imbalances** at various geographical scales.
-   **Identification of territorial clusters** based on job supply and demand.
-   **Public policy recommendations** to address mismatches between job offers and jobseekers.

## **Running the Application**

The tool is accessible by running the "labour_tightness_dashboard.ipynb" script located in `./app`. All necessary files are located in the `./data` folder.

For users wishing to reproduce the project from the beginning, the necessary scripts are provided in the `./src` directory, with detailed instructions in the README files. Some large datasets (JOCAS) need to be downloaded manually.


## **File Structure**
```
├── README.md                                       <- Main documentation of the project
├── LICENSE                                         <- Project license
├── app                                             <- Scripts to run the interactive mapping tool
├── data                                            <- All the data
│   ├── 1- Raw Data                                 <- Raw data
│   ├── 2- Formatted Data                           <- Formatted data
│   ├── 3- Final Data                               <- Final data
│   ├── linking tables                              <- Linking tables
│   └── shapefiles                                  <- Shapefiles required for mapping
├── src                                             <- Source code for data processing and analysis.
│   ├── 00_explore_jocas_missing_values.ipynb       <- Exploration of missing values in JOCAS
│   ├── 01_match_communes_with_shapefile.ipynb      <- Matching communes with shapefile
│   ├── 02_clean_rome_fap_mapping.ipynb             <- Cleaning the ROME-FAP mapping table
│   ├── 03_process_stmt_demand.ipynb                <- Processing STMT data (demand)
│   ├── 04_process_jocas_supply.ipynb               <- Processing JOCAS data (supply)
│   └── 05_compute_labour_tightness_ratio.ipynb     <- Calculating the labour market tightness ratio
├── docs                                            <- References and documents used during the project
├── reports                                         <- Methodological note + presentation slides
```


## **Contributions & Contact**

For any suggestions or to report errors, you can contact:

-   Alfonso Awadalla-Carreño : [alfonso.awadalla-carreno@polytechnique.edu](mailto:alfonso.awadalla-carreno@polytechnique.edu)
-   Cynthia Francis : [cynthia.francis@polytechnique.edu](mailto:cynthia.francis@polytechnique.edu)
-   Anahi Reyes-Miguel : [anahi.reyes-miguel@polytechnique.edu](mailto:anahi.reyes-miguel@polytechnique.edu)

Contributions and collaborations to improve the tool are welcome.
