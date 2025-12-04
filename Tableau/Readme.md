# 📊 StayCatin.com – Exploratory Data Analysis (EDA) & Tableau Dashboard

This repository contains an end-to-end Exploratory Data Analysis (EDA) project built for **StayCatin.com**, focusing on understanding listing performance, pricing patterns, host behavior, and guest interactions using **Tableau**.

---

## 📝 Problem Statement

StayCatin.com wants to analyze platform-level trends across property listings, pricing, availability, and guest reviews.  
The goal is to uncover insights that help improve:

- Listing quality  
- Host performance  
- Guest satisfaction  
- Revenue optimization  

This project performs EDA using Tableau dashboards and identifies actionable business insights.

---

## 📂 Dataset Description

The project uses three sheets provided in the dataset:

### **1. LISTING**
Includes details such as:
- Listing ID  
- Property type  
- Room type  
- Bedrooms, beds, bathrooms  
- Accommodates (capacity)  
- Host ID & host superhost status  
- Location fields  

### **2. REVIEWS**
Includes:
- Review ID  
- Listing ID  
- Reviewer ID  
- Review text  
- Review date  

### **3. PRICE_AVAILABILITY**
Includes:
- Listing ID  
- Date  
- Price  
- Availability (0 or 1)  

All sheets were cleaned and joined (using Listing ID) for analysis.

---

## 🔍 Key EDA Findings

### ⭐ **A. Property Overview**
- Total listings count  
- Distribution by property type and room type  
![Property Details Dashboard](Dashboards/PropertyDetails.png)


### ⭐ **B. Listing Characteristics**
- Distribution of bedrooms, beds, and bathrooms  
- Capacity distribution using "accommodates"  
- Relationship between **price vs capacity**  
- Outlier listings identified based on extreme pricing  
![Commodities Per Property Dashboard](Dashboards/Commodities.png)

### ⭐ **C. Top Earners**
- Top Earning Property  
- Top Earining City  
- Top Earning Hosts 
![Top Earners Dashboard](Dashboards/TopEarners.png)

### ⭐ **D. Price Vs Total Earning **
- Price Vs Total Earning for Hosts
- Price Vs Total Earning for Listed Properties
![Price Vs Total Earning Dashboard](Dashboards/TopEarners.png)
  
  
### ⭐ **E. Price Analysis**
- Price Vs Accomodates
- Price Vs ReviewRatings
- Price Vs City
- Price Vs Property Type
![Price Analysis Dashboard](Dashboards/PriceAnalysis.png)
  
---

