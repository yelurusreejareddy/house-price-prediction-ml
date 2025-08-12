# House Price Prediction using Machine Learning

capstone project (MVJ College of Engineering, VTU) — predicting house prices for localities in and around Bangalore using classical ML (Linear/Logistic Regression + collaborative filtering ideas) and a simple JSP/Servlet + MySQL web app.

> This repo packages the final report, publication, slides.
## Overview

- **Goal.** Accurately estimate house prices based on features such as area (sqft), bedrooms, bathrooms, flooring, lift/parking, furnishing, etc., plus nearby amenities (schools, hospitals, transit).  
- **Approach.** Data cleaning and feature weighting, then train/evaluate classic models (Linear & Logistic Regression; collaborative filtering conceptually to adjust for locality & amenities).  
- **App.** A 2-role web interface:
  - **Admin:** upload/view dataset, manage users.
  - **User:** query predictions by city/area/type, or by city/area/budget, or for whole city.

## Tech Stack

- **Backend:** Java 7+, JSP/Servlets (Tomcat 7+)
- **DB:** MySQL 5.7+ (example schema in `sql/`)
- **IDE:** Eclipse (any), or your favorite
- **Client:** HTML/CSS/JS

## Repository Layout

```
house-price-prediction-ml/
├─ README.md
├─ Final_Project_Report.pdf
├─ Conference_Paper.docx
├─ Phase2_Review_Slides.pptx
├─ publication/Journal_Publication.pdf
```

## Quick Start (Dev)


1. **Data**
   - Use the Admin menu to upload/view the dataset (feature list is in the report).
   - Try predictions by city/area/type, or city/area/budget.

## Results (from the study)

- Linear Regression fit the (mostly numeric) features best for the dataset analyzed.
- Logistic Regression was used for related classification-style checks.
- Incorporating locality amenities improved practical accuracy (manually validated).


## Limitations & Future Work

- Missing full Java source for Servlets/DAOs (only JSP stubs included).  
- Dataset not bundled — add your CSV and wire up upload/parse code.  
- Ideas to extend: better feature engineering, model ensembles (GBM/RF), geospatial features, SHAP for explainability, Dockerization.

## Citation

If you reference this work, please cite the included journal article (IJRASET, Aug 2021) and the project report (MVJCE/VTU).

---

### Acknowledgments

- Guide: Dr. S. Umamaheswaran (Dept. of CSE, MVJCE).  
- Team: Millee Samukcham, Riya Choudhary, M. Bhavana, Yeluru Sreeja Reddy.
