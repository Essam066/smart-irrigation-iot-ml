# Smart Irrigation System Using IoT and Machine Learning
**ML 402331 — IoT Machine Learning Project | Fall 2026/2027 | Phase 1 Proposal**

**Team members:** To be completed by the team (2–3 students).  
**Project track:** Hardware track — real sensor data collected using an ESP32-based device.

## 1. Project idea and intended user
This project proposes a low-cost smart irrigation prototype for a person caring for a potted plant or a small home garden. An ESP32 microcontroller will collect soil-moisture, ambient-temperature and relative-humidity readings. A machine-learning model will classify the current plant-watering state as either “needs watering” or “does not need watering.” The system is intended to support a timely watering decision and reduce avoidable overwatering or underwatering. The Phase 1 scope is the project design and setup plan; device construction and full data collection belong to later phases.

## 2. Problem statement
People often water plants using fixed schedules or visual guesses. These approaches may not reflect the actual moisture condition of the soil or changes in the surrounding environment. The project addresses the problem of making a consistent, sensor-informed watering decision for one selected potted plant. The proposed system will use measured environmental and soil variables to estimate whether watering is currently required. The prototype will be evaluated on data collected from its own sensors, rather than relying only on a public dataset.

## 3. Research question and objective
**Research question:** Can an IoT-based machine-learning system accurately classify whether a selected potted plant needs watering using soil-moisture, temperature and relative-humidity readings?

**Objective:** Design an ESP32 sensor system, collect at least 500 labeled readings, and prepare a reproducible data pipeline for a binary classification task. The target is to achieve a useful and measurable classification result; no performance result is claimed in Phase 1.

## 4. Machine-learning task, target and planned features
- **Task type:** Supervised binary classification.
- **Target label:** `needs_watering`: 1 = needs watering; 0 = does not need watering.
- **Feature 1:** Soil-moisture sensor reading (calibrated raw value or converted percentage).
- **Feature 2:** Ambient temperature in °C from DHT22.
- **Feature 3:** Relative humidity in % from DHT22.
- **Feature 4:** Timestamp-derived hour of day (optional planned feature).

## 5. Data collection and labeling plan
The ESP32 will log one record every 10 minutes while the plant passes through several natural drying and watering cycles. The target is at least 500 valid rows, with each row containing a timestamp, soil-moisture reading, temperature, humidity and label. Before collection, the soil sensor will be calibrated in the selected soil by recording its readings in dry and thoroughly watered conditions. A plant-specific watering threshold will be agreed using the plant-care guidance and checked by physically inspecting the soil. Each record will be labeled 1 when the calibrated soil condition and inspection indicate watering is required, and 0 otherwise. The same labeling protocol will be applied consistently and documented. Invalid sensor readings will be flagged rather than silently treated as valid data.

## 6. Hardware components and estimated cost
The following preliminary bill of materials uses indicative Jordanian retail listings where available. Prices may change and items such as tubing, a small pump and wiring should be confirmed with the supplier before purchase.

| Component | Purpose | Estimated cost (JOD) |
|---|---|---:|
| ESP32 development board | Microcontroller, Wi-Fi and sensor logging | 7.00 |
| Capacitive soil-moisture sensor | Measures soil moisture | 3.00–5.00 |
| DHT22 sensor | Measures temperature and relative humidity | 3.50–3.85 |
| 1-channel relay module | Switches the pump (later prototype stage) | 2.00–3.00 |
| 5V mini water pump + tubing | Moves water to the plant (later prototype stage) | 4.00–6.00 (estimate) |
| Breadboard and jumper wires | Temporary circuit connections | 3.00–4.00 (estimate) |
| 5V power supply / USB cable | Powers the board and pump as appropriate | 2.00–4.00 (estimate) |
| **Estimated total** | Indicative; final total depends on selected parts | **24.50–32.85 JOD** |

## 7. Software tools and setup
The planned software stack is Arduino IDE (or ESP32-compatible C++ tooling) for sensor acquisition; Python 3, Google Colab, pandas, NumPy, Matplotlib and scikit-learn for data handling and machine learning; and GitHub for version control and team collaboration. A shared repository will contain the proposal, starter notebook and later project code. The Phase 1 starter notebook is a separate course setup exercise: it loads the public diabetes dataset bundled with scikit-learn and runs a simple linear-regression example as required by the project brief. This regression exercise is not the final irrigation classifier.

## 8. Related work
1. Challa, L. P., Singh, C. D., Rao, K. V. R., Subeesh, A., & Srilakshmi, M. (2024). *Prediction of soil moisture using machine learning techniques: A case study of an IoT-based irrigation system in a naturally ventilated polyhouse.* Irrigation and Drainage, 73(3), 1138–1150. https://doi.org/10.1002/ird.2933
2. *Spatiotemporal modeling to predict soil moisture for sustainable smart irrigation.* (2023). Internet of Things, 21, 100671. https://doi.org/10.1016/j.iot.2022.100671
3. Nsoh, B., et al. (2024). *Internet of Things-Based Automated Solutions Utilizing Machine Learning for Smart and Real-Time Irrigation Management: A Review.* Sensors, 24(23), 7480. https://doi.org/10.3390/s24237480

## 9. Phase 1 setup status and limitations
The team will create one shared GitHub repository and use the included Colab-ready starter notebook. Team member names and contribution details must be added by the students. The hardware prices are estimates, not quotations. The instructor must approve the project idea and hardware track as required by the course. This document intentionally covers Phase 1 only; device construction, the 500-row collected dataset, baseline classification, cross-validation, ensemble models and deployment are outside this submission.
