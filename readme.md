![logo_ironhack_blue 7](https://user-images.githubusercontent.com/23629340/40541063-a07a0a8a-601a-11e8-91b5-2f13e4e6b441.png)

# Lab | Tableau - Python Integration with TabPy

For this lab, we will be using the Airbnb dataset to demonstrate Python integration with Tableau through TabPy. This dataset contains Airbnb listing information including prices, locations, reviews, and availability data. You can download it from the **[Airbnb Lisitings Dataset](./dataset/airbnb_listings.csv)**

In this lab we are going to explore how to enhance Tableau's analytical capabilities by integrating Python code directly into calculated fields using TabPy to perform advanced analytics on Airbnb housing data.

## Context

**Important Note about TabPy Availability:**

It's possible to try TabPy for evaluation purposes. You can download a **14-day free trial of Tableau Desktop**, which includes TabPy functionality. 

**Correction**: **Tableau Public does NOT support TabPy integration**. TabPy requires:
- Tableau Desktop (available with 14-day free trial)

**Alternative for Free Users**: If you want to use Python analytics with Tableau Public, you can:
1. Process your data with Python scripts outside of Tableau
2. Export the results to CSV files
3. Import the processed data into Tableau Public for visualization

## Prerequisites

Before starting this lab, ensure you have:
- Tableau Desktop (14-day trial or licensed version)
- Python 3.6+ installed on your system
- TabPy server installed and running

### TabPy Setup Instructions:

1. **Install TabPy**:
   ```bash
   pip install tabpy
   ```

2. **Start TabPy Server**:
   ```bash
   tabpy
   ```
   (Server will run on localhost:9004)

3. **Connect Tableau to TabPy**:
   - Help → Settings and Performance → Manage Analytics Extension Connection
   - Server: localhost, Port: 9004
   - Test Connection and Save

### Instructions

#### Part 1: Basic Python Integration

1. **Connect to the Airbnb dataset** from [LINK](https://public.tableau.com/app/sample-data/sample_-_superstore.xls)**.

2. **Create a High-Price Property Indicator**:
   - Create a calculated field named "High Price Indicator"
   - Use `SCRIPT_BOOL` to identify properties with prices above $100

3. **Create a Property Category Field**:
   - Create a calculated field named "Property Category"
   - Use `SCRIPT_STR` to categorize properties based on price ranges

#### Part 2: EXTRA OPTIONAL 

##### Mathematical Calculations with Python

4. **Create a Price Per Review Score**:
   - Create a calculated field named "Price Per Review"
   - Use SCRIPT_REAL to calculate efficiency ratio


5. **Create an Availability Score**:
   - Create a calculated field named "Availability Score" 
   - Use SCRIPT_INT to convert availability to a 1-5 rating scale

<br>

**Hints**:

- **Data Cleaning**: Check for null values in Price and Name fields before applying Python functions
- **Testing**: Start with simple calculations and gradually build complexity
- **Debugging**: If a Python script fails, check the syntax and ensure all field references are correct


## Deliverables

- `main.txt` file with a link to your Tableau Public workbook.
- `Readme-functions-explained.md` file with a brief summary (2-3 sentences) of the main `TabPy` functions implemented. 

## Submission

Upon completion, add your deliverables to git. Then commit git and push your branch to the remote.