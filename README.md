# House Price Prediction using Machine Learning

Undergrad capstone project (MVJ College of Engineering, VTU) — predicting house prices for localities in and around Bangalore using classical ML (Linear/Logistic Regression + collaborative filtering ideas) and a simple JSP/Servlet + MySQL web app.

> This repo packages the final report, publication, slides, and starter webapp stubs that mirror what’s described in the docs. If you still have the full Java/Servlet project, drop the remaining source into `webapp/` (see structure below).

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

> The original docs mention JDK 1.7/Tomcat 7 and MySQL 5.0. Modern JDK 8/11 and Tomcat 9 also work, but keep JDBC drivers in sync.

## Repository Layout

```
house-price-prediction-ml/
├─ README.md
├─ LICENSE
├─ .gitignore
├─ docs/
│  ├─ report/Final_Project_Report.pdf
│  ├─ paper/Conference_Paper.docx
│  ├─ slides/Phase2_Review_Slides.pptx
│  └─ publication/Journal_Publication.pdf
├─ webapp/
│  └─ jsp/
│     ├─ index.jsp           # User/Admin login popup
│     ├─ Adminhome.jsp       # Admin side nav + iframe
│     └─ Adduser.jsp         # Admin: add user form
└─ sql/
   ├─ schema.sql             # Minimal tables (adminlogin, userlogin)
   └─ README.md              # Notes on DB setup
```

## Quick Start (Dev)

1. **MySQL setup**
   - Create a database (e.g., `realestate_ml`) and user with privileges.
   - Run `sql/schema.sql` to create minimal tables.
   - If you’ll run the JSP as-is, adjust JDBC URL/credentials to match your DB in the Servlet layer (placeholders provided).

2. **Tomcat / App**
   - Place `webapp/` contents inside your Dynamic Web Project (`src/main/webapp` for Maven; or WebContent/ for classic Eclipse).
   - Ensure the MySQL JDBC driver JAR is on the server classpath.
   - Deploy to Tomcat and visit `http://localhost:8080/` for the login page.

3. **Data**
   - Use the Admin menu to upload/view the dataset (feature list is in the report).
   - Try predictions by city/area/type, or city/area/budget.

## Results (from the study)

- Linear Regression fit the (mostly numeric) features best for the dataset analyzed.
- Logistic Regression was used for related classification-style checks.
- Incorporating locality amenities improved practical accuracy (manually validated).

Full details and screenshots are in the docs under `docs/`.

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
