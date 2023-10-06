# Data_Visualization_Challenge

## Description

**Description:** A new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer. As a senior data analyst at the company, you've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.
The task was generating all of the tables and figures needed for the technical report of the clinical study. They have also asked you for a top-level summary of the study results.

---

## Dependencies and Setup

import matplotlib.pyplot as plt

import pandas as pd

import scipy.stats as st


- Study data files
  
  mouse_metadata_path = "/Users/leahmuliokela/Documents/Resources/Mouse_metadata.csv"
  study_results_path = "/Users/leahmuliokela/Documents/Resources/Study_results.csv"

- Read the mouse data and the study results
  
  mouse_metadata = pd.read_csv(mouse_metadata_path)
  study_results = pd.read_csv(study_results_path)

- Combine the data into a single DataFrame
  
  study_data_complete = pd.merge(study_results,mouse_metadata,how="left",on="Mouse ID")

---

## Generating Summary Statistics

- Generated a summary statistics table of mean, median, variance, standard deviation, and SEM of the tumor volume for each regimen
- Generated a bar plot showing the total number of rows (Mouse ID/Timepoints) for each drug regimen using Pandas.
- Generate a pie plot showing the distribution of female versus male mice using Pandas
- Generated a pie plot showing the distribution of female versus male mice using pyplot
- Calculated the final tumor volume of each mouse across four of the treatment regimens
- Generated a box plot that shows the distrubution of the tumor volume for each treatment group
- Generated a line plot of tumor volume vs. time point for a single mouse treated with Capomulin
- Generated a scatter plot of mouse weight vs. the average observed tumor volume for the entire Capomulin regimen
- Calculated the correlation coefficient and a linear regression model 
