# ClimateAnalysisMilkweed
A species distribution model of Ascleipias syriaca and speciosa in the United States of America using climate data and projection for future based on climate change models.

Link to Annotated Bibliography and project notes: https://docs.google.com/document/d/1EEXL6ebBq5HCnoB9HkluoOjj4xjTCCo2R4pnNthjMo8/edit?pli=1&tab=t.0

# Pipeline (subject to edits):
## Collect and clean occurrence data
- Past climate data: CO2 emissions, precipitation, warm and cold temperatures
- Asclepias syriaca and speciosa sightings with geographical location
## Feature Engineering
- Extract bioclimactic variables
- Create pseudo-absences (i.e. generate background points to train model)
## Training & Testing Model
- Split Training/Test Sets
- Build Ensemble Model (GLM model for climate) --> get feature importances for data visualization
- Determine accuracy with auc(roc_curve) with target >0.7
## Deliverable:  climate change with species distribution
- Download future bioclim data (e.g., RCP 8.5, 2050s from WorldClim) → predict on that stack using the ensemble.
- Create shiny web app using leaflet to host climate show projected distributions – probability of species occurring in a region. 
- Dropdown menus: sort by species, severity of climate scenario, when hovering show coordinate and predicted value
