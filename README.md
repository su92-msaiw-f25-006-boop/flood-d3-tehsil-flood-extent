# Flood-Prone Tehsils of Pakistan: Monsoon Inundation and Spatial Clustering (2022–2025)

This repository contains geospatial datasets and machine learning classification models evaluating monsoon flood susceptibility and spatial clustering across 577 tehsils and 160 districts in Pakistan (2022–2025). Based on VIIRS satellite detections calibrated against UNOSAT inundation maps, it models serious flood recurrence using Getis-Ord Gi* hotspot metrics and spatial clustering attributes via Logistic Regression, Random Forest, and XGBoost classifiers.

## Folder Structure

```
flood-d3-tehsil-flood-extent/
├── 1_code/
│   └── Flood_Extent_Tehsil_Pakistan.ipynb  # Notebook: EDA, spatial clustering & classifiers
├── 2_kaggle_input/
│   ├── District_Level_Data.csv             # District-aggregated annual flood statistics
│   ├── Tehsil_Level_Data.csv               # Tehsil-level flood inundation & hotspot records
│   └── Variable_Dictionary.csv             # Metadata schema and feature definitions
├── 3_kaggle_output/
│   └── Dataset_3_Tehsil_Flood_Extent_OUTPUT.ipynb # Executed notebook with model outputs
├── 4_doc/
│   └── Dataset 3 - Flood-Prone Tehsils Pakistan - Results.docx # Experimental summary report
├── .gitignore
├── LICENSE
├── README.md
└── requirements.txt
```

## How to Run

1. **Prerequisites:** Python 3.10 or higher.
2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Notebook:**
   ```bash
   jupyter notebook 1_code/Flood_Extent_Tehsil_Pakistan.ipynb
   ```

The models evaluate temporal out-of-time splits (training on historical tehsils through 2024 and testing on 2025 monsoon impacts) to prevent temporal data leakage.

## Data Source and Licence

- **Primary Source:** Zenodo dataset *"A Multi-Resolution Geospatial Dataset of Monsoon Flood Extent and Spatial Clustering for Pakistan (2022–2025)"* by A. Umer (2026).
  - DOI: [https://doi.org/10.5281/zenodo.20100773](https://doi.org/10.5281/zenodo.20100773)
  - Underlying satellite mapping: NASA/NOAA Visible Infrared Imaging Radiometer Suite (VIIRS) cross-validated with UNOSAT (United Nations Satellite Centre) flood maps.
- **Data Licence:** Creative Commons Attribution 4.0 International ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)).
- **Code Licence:** The code in this repository is released under the [MIT License](LICENSE).

## Citation

```bibtex
@misc{anwar2026_tehsil_flood,
  author = {Shahan Anwar},
  title = {Flood-Prone Tehsils of Pakistan: Monsoon Inundation and Spatial Clustering (2022--2025)},
  year = {2026},
  publisher = {GitHub},
  howpublished = {\url{https://github.com/su92-msaiw-f25-006-boop/flood-d3-tehsil-flood-extent}}
}
```
