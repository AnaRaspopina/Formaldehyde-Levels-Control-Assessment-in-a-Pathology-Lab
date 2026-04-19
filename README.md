#  Formaldehyde Levels Control Assessment in a Pathology Laboratory Environment

**Author:** Anastasia Raspopina  
**Role:** Senior Pathologist Assistant | Data Analyst  
**Location:** Auckland, New Zealand

---

##  Project Objective

This project investigates the **ambient formaldehyde levels** in the Grossing Area of a Community Anatomic Pathology laboratory using historical data from portable measurement devices (PPM HTV-M Formaldemeters).

![meter](https://github.com/user-attachments/assets/604f23b1-b0a0-4434-9b15-6f2b67138a7c)


**The primary objectives:**

-  Understand the **patterns and variability** of formaldehyde exposure
-  Assess **environmental factors** influencing concentration (temperature, humidity, occupancy)
-  Evaluate the **reliability and limitations** of legacy measurement equipment
-  Provide **data-driven recommendations** to improve worker safety and compliance

---

##  Why It Matters

**Formaldehyde is a proven carcinogen** and potent local irritant. Continuous exposure even at low levels poses health risks, especially in environments like pathology labs.

- **WorkSafe NZ Acceptable Limit:** 0.3 ppm  
- **Recommended Safe Level:** 0.1 ppm

These thresholds apply to areas where personnel do not wear respiratory protection. Monitoring is both a **compliance requirement** and a **moral obligation** to protect healthcare workers.

---

##  Data Overview

- **Source:** CSV logs from PPM HTV-M devices (manual download)
- **Fields:**  
  - `Timestamp`  
  - `Formaldehyde concentration (ppm)`  
  - `Temperature (°C)`  
  - `Relative Humidity (%)`

>  **Known device limitations:**
> - Prone to cross-sensitivity with other reagents (ethyl alcohol, xylene)
> - Inconsistent temperature/humidity readings due to sensor age
> - Requires frequent calibration

---

## 🧹 Data Cleaning Strategy

To ensure analytical robustness, the following filters were applied:

- Removed all **formaldehyde readings > 0.5 ppm** (potential other laboratory reagent interference)
- Excluded records with **temperature < 15°C** (indicating faulty sensor or inappropriate measurement conditions)
- Excluded records with **humidity < 30%** (indicating faulty sensor or inappropriate measurement conditions)
- Dropped incomplete or clearly corrupted records

---

##  Exploratory Insights

###  Daily Trends in Formaldehyde Levels

*Shows day-to-day fluctuation in median exposure.*

![Dailyformplot](https://github.com/user-attachments/assets/1ad72a69-b3d8-4a65-8cc4-33d559ea07e6)


---

###  Formaldehyde vs. Temperature 

*Evaluates whether temperature fluctuations correlate with elevated emissions.*

![formVStemp](https://github.com/user-attachments/assets/ae6bfba0-8930-4fcb-9058-27643acbaf2f)

---

###  Formaldehyde vs. Humidity 

*Evaluates whether humidity fluctuations correlate with elevated emissions.*

![formVStemp](https://github.com/user-attachments/assets/ae6bfba0-8930-4fcb-9058-27643acbaf2f)

###  Shifts Effects

*Compare median emissions during the day and night shifts.*

![shiftsBar](https://github.com/user-attachments/assets/7ce2302a-ca14-4427-97d6-4ace5757c2b7)

---

##  Key Findings

1. **Room occupancy** is the most consistent factor influencing formaldehyde levels.
2. **Temperature** affects concentration but does not need to be kept uncomfortably low.
3. Adding more stations **may keep levels within acceptable limits**, but WorkSafe’s cap of **5 workers** remains reasonable.
4. The current formaldehyde meter is **outdated and should be upgraded** for more reliable, continuous monitoring.

---

## ✅ Recommendations

-  Transition to **modern, network-connected** sensors with real-time logging and automated calibration.
-  Evaluate ventilation efficiency during peak hours.
-  Retain the existing policy of a **maximum of 5 people** in the Grossing Area.

---

##  Disclaimer

This study involves a retrospective data analysis. The dataset was de-identified and contained **no personal or patient information**. Measurements were sourced from general-purpose monitoring instruments and not medical-grade sensors.

---

##  Contact

**Anastasia Raspopina**  
📧 AnaRaspopina@gmail.com  
🔗 [LinkedIn Profile](https://www.linkedin.com/in/ana-rasp)
