# Amsterdam Apartment Price Estimator

## Project Overview

This project develops a machine-learning model that estimates the asking price of an existing apartment in Amsterdam using its location, size, building characteristics, facilities and condition.

The project focuses exclusively on regular apartments offered for individual sale within urban Amsterdam.

## Version 1: Characteristics Model

Version 1 uses only observable apartment, building and location characteristics.

The model will produce two outputs:

1. Estimated asking price in euros
2. Estimated asking price per square metre

Price per square metre is an output of the model, not an input variable.

## Property Scope

### Included

- Existing apartments offered for individual sale
- Apartments located within urban Amsterdam
- Different apartment subtypes
- Apartments with or without outdoor space
- Apartments with different construction periods, conditions and facilities

### Excluded

- Entire houses
- Rooms
- Parking spaces sold separately
- Entire new-development projects
- New-development listings
- Properties located in Weesp

## Model Variables

### Location

- District
- Neighbourhood
- Postcode
- Latitude
- Longitude
- Distance from Amsterdam city centre
- Nearest metro station
- Distance to the nearest metro station in kilometres

### Listing Information

- Listing date

### Apartment Size and Layout

- Living area in square metres
- Number of bedrooms
- Number of rooms
- Number of bathrooms
- Number of toilets
- Apartment subtype
- Floor level
- Number of internal floors

### Outdoor Space and Storage

- Balcony availability
- Balcony area
- Terrace availability
- Terrace area
- Garden availability
- Garden area
- Storage availability
- Storage area

### Building Age and Condition

- Construction year
- Building age
- Renovation year
- Property condition

### Energy and Heating

- Energy label
- Insulation
- Glazing type
- Heating type

### Building Facilities

- Elevator
- Accessibility features
- Private parking availability

## Excluded Variables

The following information will not be used in Version 1:

- WOZ value
- Ownership or personal owner information
- Ground-lease or ownership arrangements
- VvE financial information
- Service charges
- Listing descriptions
- Listing photographs

## Data Strategy

The project will be developed in two data stages:

1. Begin with an existing static apartment dataset.
2. Consider incorporating current apartment listings later.

The first dataset will be filtered so that it contains only eligible Amsterdam apartments.

## Project Workflow

1. Create the project structure and Python environment.
2. Obtain and inspect the static apartment dataset.
3. Clean and validate the data.
4. Filter the dataset to the approved property scope.
5. calculate location and metro-distance variables.
6. Explore Amsterdam apartment price patterns.
7. Prepare the variables for machine learning.
8. Train the characteristics model.
9. Evaluate asking-price and price-per-square-metre predictions.
10. Save the trained model, results and visualisations.

## Planned Repository Structure

```text
Real-Estate-Pricing-Project/
├── data/
│   ├── raw/
│   └── processed/
├── models/
├── notebooks/
├── outputs/
│   ├── figures/
│   └── predictions/
├── src/
│   ├── __init__.py
│   ├── data_loader.py
│   ├── data_cleaning.py
│   ├── feature_engineering.py
│   ├── model.py
│   └── evaluation.py
├── .gitignore
├── main.py
├── README.md
└── requirements.txt