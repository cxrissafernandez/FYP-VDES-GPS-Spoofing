# FYP: Secure Monitoring of Ship Location using VDES Technology and Satellite Communication

## 1. Repository Structure and Milestones

This repository serves as **Appendix A** of the Interim Report, documenting the project's milestones and progression from initial Python proof-of-concept to the finalized C-language implementation.

| Folder | Content | Milestone Achieved |
| :--- | :--- | :--- |
| `01_Python_Prototype/` | **AIS Decoder (Jupyter Notebook)** | Functional validation of the core 6-bit un-armouring and message parsing logic and mapping data. Includes static HTML for ease of view. **Contains the full source code for the original and refined scripts (in both html and .ipynb)** |
| `02_C_Implementation/` | **AIS Decoder (C-Language)** | Successful conversion of the prototype logic to the industrial embedded C environment. **Contains the full source code snapshots (ais_decoder_C & refined_ais_decoder_C).** |
| `03_Visualisation/` | **Mapping & Output Screenshots** | Visual proof-of-concept of decoded data accuracy, map outputs, and console results (terminal/output cell screenshots). |
| `04_Sample_Data/` | **NMEA Input / CSV Output** | Source data used for testing and validation, and results. |

---

## 2. Technical Validation and Verification

### 2.1. Decoder Robustness and Data Completeness (AIS Decoder_Python (120925) vs. Refined AIS Decoder_Python (081125) Insight)

The initial decoding effort identified two critical requirements: robustness against malformed data and ensuring the output retained full static vessel information.

* **Non-Standard Filtering:** Validation logic was implemented to accurately identify and filter **non-standard AIS message types (28-63)** that are outside the ITU-R M.1371 standard, preventing corrupted data contamination in the subsequent analysis pipeline.
* **Field Completeness:** The final Python and C decoders were configured to return a consistent array of **35 fields** (often referred to in development as AIS Decoder_Python (081125)). This was necessary because preliminary versions (AIS Decoder_Python (120925)) only outputted 17 core navigational fields, **omitting essential static data (Ship Name, IMO, Call Sign, Ship Dimensions)** found in auxiliary AIS messages (Type 5, 19, 24). The 35-field structure ensures data completeness for both ship identification and detailed visualization.

### 2.2. Verification Files and Interactive Access

The following files allows one to verify the project's functionality and results directly:

| Verification Component | File Location | Functional Description |
| :--- | :--- | :--- |
| **Latest Interactive Python Code & Map** | `01_Python_Prototype/Refined AIS Decoder_Python (081125).ipynb` | Download and open this `.ipynb` file in a Jupyter environment (e.g., **VS Code or Jupyter Lab**) to execute the code cells and interact directly with the live map output. |
| **Decoded Data Sample** | `04_Sample_Data/nmea-sample_Refined_AIS_Decoder_C_081125` | Provides the structured 35-field CSV output data for numerical review. Other sample data is also available in the same folder |
| **Static Map Output** | `03_Visualisation/Mapping on Jupyter` | Provides the static map output with the data shown when a vessel marker is clicked (screenshot). |
| **Full C Code Snapshot** | `02_C_Implementation/` | Contains the screenshot of the full C code of both versions for ease of review. |

### 2.3. Functional Equivalence (C vs. Python)

The integrity of the conversion from the Python prototype to the C implementation is proven by the side-by-side console output comparison in **Figure 5** of the report, demonstrating functional equivalence.

* **To Run Python Prototype:** Download and open the relevant `.ipynb` file in a Jupyter environment to execute the code cells. This repository contains both versions of file structures to show the difference in the data returned.
* **To Review Latest C Implementation:** The source code in `02_C_Implementation/refined_ais_decoder_C.c` can be compiled and run in a local C environment to confirm functional equivalence.
* **Data Sources:** The necessary sample input data files are available in `04_Sample_Data/L4_All_AIS_Messages.txt` and `04_Sample_Data/nmea-sample_AIS_Messages`. **Note: Update the file paths for input and output before running the code locally.**

---

### Contact

As this is my first time using GitHub, if you are unable to open any of the files, do drop me an email and I will send the files over directly! 
