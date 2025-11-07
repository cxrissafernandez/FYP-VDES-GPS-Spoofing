# FYP: Secure Monitoring of Ship Location using VDES Technology and Satellite Communication

## Project Overview

This repository contains the validated source code and supporting data for the Final Year Project Interim Report on **Secure Monitoring of Ship Location using VDES Technology and Satellite Communication**. The project aims to design a system to detect **GPS spoofing** in Automated Identification System (AIS) messages by comparing reported ship locations against the satellite payload's verifiable telemetry data.

if unable to open any of the files, do drop me an email! thanks!

## 1. Repository Structure and Milestones

The folders below reflect the project's milestones, the progression from initial proof-of-concept to the final C-language implementation:

| Folder | Content | Milestone Achieved |
| :--- | :--- | :--- |
| `01_Python_Prototype/` | **AIS Decoder (Jupyter Notebook)** | Functional validation of the core 6-bit un-armouring and message parsing logic and mapping data. Includes static HTML for ease of view |
| `02_C_Implementation/` | **AIS Decoder (C-Language)** | Successful conversion of the prototype logic to the embedded C environment. |
| `03_Visualisation/` | **Mapping & Output** | Visual proof-of-concept of decoded data accuracy. |
| `04_Sample_Data/` | **NMEA Input / CSV Output** | Source data used for testing and validation, and results. |

---

## 2. Verification and Code Access

This repository serves as **Appendix A** of the Interim Report, containing all source code listings.

### 1. Proof of Concept Verification

If one needs to verify the functionality, please refer to the following:

* **Full Python Code:** The file `01_Python_Prototype/AIS Deoder.html` can be downloaded and opened directly in any web browser to view the full code + interactive map.
* **Decoded Data Sample (Figure 3):** The file `04_Sample_Data/L4_NMEA_Decoded.txt` provides the structured output data for numerical review.
* **Static Map Output (Figure 4):** The file `03_Visualisation/Mapping on Jupyter` provides the static map output with the data shown when a vessel is clicked.
* **Full C Code:** The file `03_Visualisation/code-snapshot, c code` provides a screenshot of the full C code for ease of view.

### 2. Functional Equivalence (C vs. Python)

The successful C-language conversion is proven by the side-by-side console output comparison in **Figure 5** of the report. The source code for both programs is available here:

* **To Run Python Prototype:** Download and open the `.ipynb` file in a Jupyter environment (e.g., VS Code or Jupyter Lab) to execute the code cells.
* **To Review C Implementation:** The code in `02_C_Implementation/` can be compiled and run in a local C environment (e.g., VS Code or command line) to check functional equivalence. 

The sample input data to be used can be downloaded from `04_Sample_Data/L4_All_AIS_Messages`. Update the path files for input and output before running the code.
