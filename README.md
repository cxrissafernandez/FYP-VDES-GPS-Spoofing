# FYP-VDES-GPS-Spoofing

## Project Overview

This repository contains the validated source code and supporting data for the Final Year Project Interim Report on **Secure Monitoring of Ship Location using VDES Technology and Satellite Communication**. The project aims to design a system to detect **GPS spoofing** in Automated Identification System (AIS) messages by comparing reported ship locations against the satellite payload's verifiable telemetry data.


## 1. Repository Structure and Milestones

The folders below reflect the project's milestones, allowing reviewers to verify the progression from initial proof-of-concept to the final C-language implementation:

| Folder | Content | Milestone Achieved |
| :--- | :--- | :--- |
| `01_Python_Prototype/` | **AIS Decoder (Jupyter Notebook)** | Functional validation of the core 6-bit un-armouring and message parsing logic and mapping data. Includes static HTML for ease of view |
| `02_C_Implementation/` | **AIS Decoder (C-Language)** | Successful conversion of the prototype logic to the embedded C environment. |
| `03_Visualization/` | **Mapping & Output** | Visual proof-of-concept of decoded data accuracy. |
| `04_Sample_Data/` | **NMEA Input / CSV Output** | Source data used for testing and validation, and results. |

---

## 2. Verification and Code Access

This repository serves as **Appendix A** of the Interim Report, containing all source code listings.

### 1. Proof of Concept Verification

If one needs to verify the functionality, please refer to the following:

* **Static Map Output (Figure 2):** The file `03_Visualization/final_map_output.html` can be opened directly in any web browser to view the decoded vessel tracks without needing to run the code.
* **Decoded Data Sample (Table A.1):** The file `04_Sample_Data/L4_NMEA_Decoded.csv` provides the structured output data for numerical review.

### 2. Functional Equivalence (C vs. Python)

The successful C-language conversion is proven by the side-by-side console output comparison in **Figure 3** of the report. The source code for both programs is available here:

* **To Run Python Prototype:** Download and open the `.ipynb` file in a Jupyter environment (e.g., VS Code or Jupyter Lab) to execute the code cells.
* **To Review C Implementation:** The code in `02_C_Implementation/` can be compiled and run in a local C environment (e.g., VS Code or command line) to check functional equivalence.
