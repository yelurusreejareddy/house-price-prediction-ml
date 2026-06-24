# house-price-prediction-ml

Undergraduate capstone project predicting residential house prices for localities
in and around Bangalore using classical ML models and a two-role web application.
Published in IJRASET, August 2021.

## Files Included

- Publication.pdf - IJRASET published paper (August 2021)
- MajorProject_Report.pdf - full project report with methodology and results
- Paper(Major_project).docx - conference paper draft
- Phase 2_review.pptx - project review presentation

Note: Dataset and web application source code not included in this repo, will be provided upon request.

## Problem

Residential property prices in Bangalore vary significantly by locality, size,
and available amenities. The goal was to build a model that accurately estimates
price based on structured property features and neighborhood context.

## Approach

- Data collection and cleaning on Bangalore housing listings
- Feature engineering on area (sqft), bedrooms, bathrooms, floor type,
  lift/parking availability, furnishing level, and locality amenities
  (schools, hospitals, transit proximity)
- Locality-based weighting to capture neighborhood price effects
- Trained and compared Linear Regression and Logistic Regression
- Built a two-role web application (Admin: dataset management and user control,
  User: price queries by area/type, area/budget, or full city view)

## Techniques Used

- Data cleaning, normalization, and feature weighting
- Linear Regression for continuous price estimation
- Logistic Regression for price-range classification
- Collaborative filtering concepts applied to locality and amenity adjustment
- Web app built with JSP/Servlets + MySQL for real-time prediction queries

## Stack

Python, scikit-learn, pandas, numpy, Java, JSP/Servlets, MySQL

## Results

Linear Regression performed best on the numeric feature set.
Incorporating locality amenity features improved practical prediction accuracy.
Findings published in IJRASET Volume 9, Issue 8, August 2021.

## Goal

To build an accessible price prediction tool for homebuyers and validate
the approach through peer-reviewed academic publication.

---

Acknowledgments: Dr. S. Umamaheswaran (Dept. of CSE, MVJCE) - project guide.
Team: Yeluru Sreeja Reddy, Millee Samukcham, Riya Choudhary, M. Bhavana.
