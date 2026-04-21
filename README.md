# CIVE-202---Project-4
This project is to evaluate the risks of natural disasters. Our sensitivity analysis was developed using a risk assessment that differs from the NRI results. Assessment of risk performed by NRI was compared to our assessment to find biases within NRI standards. We performed the comparison using Vermont and Maine at the Census Tract level. 

---
## Repository Structure

### Raw Data
`Links:`

- [Maine_data](Maine.csv)
- [Vermont_data](Vermont.csv)
- [NRI_Hazard_Info](NRI_HazardInfo.csv)
- [NRI_DataDictonary](NRIDataDictionary.csv)
- [NRI_Metadata](NRI_metadata_December2025.pdf)
- [Notebook(Project_4_Code)](CIVE202_Spring2026_Project4_Group11_PythonCode.ipynb)
  
  `NRI_Table_CensusTracts file was also used in the code, but the file is too large to upload here.`

---
## User Guide

### 1. Program Overview
  Using both NRI’s original definitions for risk and our new proposed definitions, Risk Averse, LLC has asked our team to conduct an analysis of the risk of natural disasters in two states of our choice. The states we conducted our analysis on are Maine and Vermont. The program combines multiple datasets together, handles missing or NA values, generates two figures showing risk scoring by NRI and our definitions of risk, and generates one map using GeoPandas. 

**Example:**
This example goes through how to join multiple datasets together from the NRI database and how to handle missing or NA values in the dataset. We will be doing Maine for this example.

### 2. Methods
1. First filter the large dataset to only contain data for the state of maine. The code will look like this: ""maine_tracts = all_tracts[all_tracts["STATE"] == "Maine"]"., then convert the filtered data to a .csv file using the ".to_csv" command.
2. Load the NRI and SVI datasets for Maine using the "pd.read_csv" command.
3. Merge the two datasets together using "pd.merge" and remove any duplicates.
4. Print the data set, stitching on ".isna()" to the end of the data file name to handle the missing information.
5. Some columns will be missing, so it is best to remove those columns. To do this, use the ".dropna" command and then print the new, filtered dataset.

---
## Project Goals
The goals of this project were outlined with the use of a Gantt Chart. The link is here:

- [Gantt_Chart](CIVE202_Spring2026_Project4_Group11_GanttChart.xlsx)

---
## Project Documentation
`Links:`

The project deliverables were planned and tracked using an engineering time sheet to ensure organized progress throughout the project.
- [Time_Sheet](CIVE202­_Spring2026_Project4_Group11_EngineeringTimeSheet.xlsx)

Additional project documentation:
- [Annotated_Code_Document](CIVE202_Spring2026_Project4_Group11_ACD.xlsx)
- [Scope_of_Work](CIVE202_Spring2026_Project4_Group11_ScopeofWork.docx)
- [Written_Report](CIVE202_Spring2026_Project4_Group11_WrittenReport.docx)
