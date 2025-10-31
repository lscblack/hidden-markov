---

# **Human Activity Recognition with HMM**

## **Purpose**

This project aims to detect human activities — **walking, standing, running, and jumping** — using data collected from smartphone **accelerometer** and **gyroscope** sensors. The model uses a **Hidden Markov Model (HMM)** to classify activities based on motion signals.

We collected our **own sensor data** using the **Sensor Logger app**, ensuring each activity was recorded under realistic conditions.

---

## **Dataset**

* **Data collected:** Accelerometer and gyroscope signals
* **Sampling rate:** 50–100 Hz
* **Activities:** Jumping, Running, Standing, Walking
* **Each student** contributed their own activity samples
---

---
## **Project Structure**

📂 Human_Activity_Recognition_HMM

├── 📁 data/# Raw CSV files collected from sensors

├── 📁 dataset/       # Cleaned and combined datasets per activity

├── 📁 notebook/      # Jupyter notebook 

│
└── README.md    #README file

---



## **Model**

We trained and tested a **Hidden Markov Model (HMM)** to classify activities based on time-series data patterns.

---

## **Results**

| State (Activity) | Number of Samples | Sensitivity | Specificity | Overall Accuracy |
| ---------------- | ----------------- | ----------- | ----------- | ---------------- |
| Jumping          | 22                | 0.4091      | 1.0000      | 0.87             |
| Running          | 37                | 0.9730      | 1.0000      | 0.99             |
| Standing         | 24                | 1.0000      | 0.8553      | 0.89             |
| Walking          | 17                | 1.0000      | 0.9639      | 0.97             |

**Overall Accuracy:** 0.8475

| Metric               | Precision | Recall | F1-Score | Support |
| -------------------- | --------- | ------ | -------- | ------- |
| Jumping              | 1.00      | 0.41   | 0.58     | 22      |
| Running              | 1.00      | 0.97   | 0.99     | 37      |
| Standing             | 0.69      | 1.00   | 0.81     | 24      |
| Walking              | 0.85      | 1.00   | 0.92     | 17      |
| **Average Accuracy** |           |        | **0.86** | 100     |

---

## **Challenges**

One main challenge we faced was **inconsistent recordings**. Some activities (like jumping) had **low recall** due to unstable sensor placement, leading to several **zero or missing readings**.
We had to **re-record some activities** to improve the dataset quality and ensure better model performance.

---

##  Collaboration and GitHub Contribution

This project was completed as a **group effort**.We both contributed equally to all stages of the project, with approximately **50% effort each**. Together, we recorded accelerometer and gyroscope data for all four activities using the Sensor Logger app, ensuring that our samples were consistent and well-labeled before analysis.

### Our Main Roles

- **We both:** participated in data recording, labeling, and validation to ensure reliable input for the model.  
- **Nelly Iyabikoze:** focused on data cleaning, preprocessing, and dataset organization. She also contributed to report writing, especially in the background, motivation, and data description sections, and helped verify the accuracy of the model results and visualizations.  
- **Loue Sauveur Christian:** focused on feature extraction, HMM model implementation, and evaluation. He developed the training and testing scripts, created visualizations (confusion matrix and transition heatmap), and contributed to interpreting the model outputs.  

Overall, we worked collaboratively throughout the project, supported each other’s tasks, and maintained balanced contributions in both coding and documentation.

## **Conclusion**

The HMM model successfully recognized human activities with an **overall accuracy of about 85%**. Despite challenges with noisy or incomplete sensor data, the project demonstrates that HMMs can effectively classify basic human motions using smartphone sensors.

---
