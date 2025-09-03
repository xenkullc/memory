I need you to act as an expert AI developer. Your task is to create two initial template scripts for my "Mega Millions Pick Deep Learning Adapt" project. These scripts will serve as the base `v1.001` for the system to build upon.

### **1. The Goal and Problem Context**

I have two analyzer scripts, `mm_deep_analyzer_inorder.py` and `mm_deep_analyzer_asdrawn.py`, which are designed to analyze lottery data, calculate new algorithm weights, and then generate a new, optimized prediction script (e.g., `mm_predictions_1.002.py`).

The problem is that these analyzers work by finding the *previous* version (e.g., `mm_predictions_1.001.py`), reading its code as a template, and then injecting the new weights. Since no initial `mm_predictions_1.001.py` file exists, the process fails.

Your task is to create the two necessary `mm_predictions_1.001.py` template files. One will be for the "Numbers In Order" part of the project, and the other for the "Numbers As Drawn" part.

### **2. Reference and Source Scripts**

I am providing all the necessary reference scripts. You must adapt the logic from the **Powerball** prediction scripts to create the new **Mega Millions** versions.

* **Reference for "In Order" version:** `pb_predictions_1.009.py` (This script sorts the main numbers).
* **Reference for "As Drawn" version:** `pb_predictions_1.001.py` (This script preserves the temporal/draw order of the main numbers).
* **Analyzer Scripts for Context:** `mm_deep_analyzer_inorder.py` and `mm_deep_analyzer_asdrawn.py` (You can review these to see how they will interact with the templates you create).

*(The full code for all four scripts that I provided to you has been attached for the AI model's perusal).*

### **3. Task 1: Create the "Numbers In Order" Template**

Generate a complete Python script named `mm_predictions_1.001.py` that is based on `pb_predictions_1.009.py`. This script must be fully converted to work for Mega Millions.

**Specific conversion requirements:**

1.  **Game Rules:**
    * Change the main number range from **1-69** to **1-70**.
    * Change the special ball range from **1-26** to **1-24**.
2.  **Terminology and Naming:**
    * Replace all instances of "Powerball" and "PB" with "Mega Millions" and "MB" respectively (in comments, print statements, variable names, and file names like `PB.csv` -> `MB.csv`).
    * Update the output text file to be `megamillions_prediction.txt` or similar, and change the title inside it.
3.  **Versioning:**
    * Set the version number in the header and in the `save_prediction` function call to `1.001`.
4.  **Functionality:**
    * **Crucially, ensure this version sorts the five main numbers before they are displayed and saved**, just like the `pb_predictions_1.009.py` reference script does (i.e., the `predicted_numbers.sort()` line must be active).

### **4. Task 2: Create the "Numbers As Drawn" (Temporal) Template**

Next, generate a second, separate script, also to be named `mm_predictions_1.001.py` (I will place it in a different directory). This script should be based on `pb_predictions_1.001.py`.

**Specific conversion requirements:**

1.  **Game Rules & Terminology:** Apply the exact same Mega Millions rule and terminology conversions as listed in Task 1.
2.  **Versioning:** Set the version number to `1.001`.
3.  **Functionality:**
    * **This is the key difference:** This version **must not sort** the five main numbers. It must preserve their "as drawn" or temporal order.
    * Locate the `predicted_numbers.sort()` line and ensure it is **commented out**, with a note like `# TEMPORAL ORDER - DO NOT SORT`. This will align with the modification logic found in the `mm_deep_analyzer_asdrawn.py` script.

Please provide the full code for each of the two scripts separately.
