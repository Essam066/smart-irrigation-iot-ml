# Smart Irrigation System Using IoT and Machine Learning

**Course:** ML 402331 — IoT Machine Learning Project  
**Phase:** 1 — Idea, Problem and Setup  
**Track:** Hardware

## Project question
Can an IoT-based machine-learning system accurately classify whether a selected potted plant needs watering using soil-moisture, temperature and relative-humidity readings?

## Phase 1 files
- `Phase1_Proposal_Smart_Irrigation.pdf` — two-page proposal and preliminary bill of materials.
- `Phase1_Starter_Linear_Regression.ipynb` — Colab-ready course starter notebook.
- `BILL_OF_MATERIALS.md` — preliminary hardware list and estimated costs.

## Planned hardware
ESP32 development board, capacitive soil-moisture sensor, DHT22 temperature/humidity sensor, and optional relay/pump components for the later physical prototype.

## Planned ML task
Supervised binary classification:
- `needs_watering = 1`: watering is required.
- `needs_watering = 0`: watering is not required.

Planned features: soil moisture, ambient temperature, relative humidity, and optionally hour of day.

## Data plan
Collect at least 500 labeled sensor rows. Calibrate the soil-moisture sensor in the selected soil and apply one documented plant-specific labeling protocol consistently. The target dataset will be collected from the team's own device in a later phase.

## Starter notebook note
The included notebook uses scikit-learn's public diabetes regression dataset to run the Phase 1 linear-regression setup exercise. It is not the irrigation classifier.

## Before submission
1. Add the actual team member names to the proposal.
2. Open the notebook in Google Colab and run all cells.
3. Obtain instructor approval for the hardware track and project idea.
4. Submit using the course's required ZIP naming convention: `ML402331_Phase1_<TeamName>.zip`.
