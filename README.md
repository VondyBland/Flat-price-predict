# Moscow Flat's Price Prediction Regression

## Purpose of it
The purpose of this project is to develop a model that can correctly predict the cost of apartments in Moscow.

Analysis and modeling of real estate data are of great practical importance, as they allow both consumers and sellers to make more informed decisions. Especially it can be helpful, deciding on which factors to base your prices on estate.

## Structure


bash
Copy code
/
├── data/                               # Data Directory

  │   ├── housing.csv                   # Data
  
├── notebooks/                          # Jupyter notebooks

│   ├── estate_price_prediction.ipynb   # Data analysis, data processing and model building

├── README.md                           # README

├── requirements.txt                    # Libraries

## Installing required libraries

bash
Copy code
pip install -r requirements.txt

## Data
A set of data on the sale of real estate in Moscow in 2014 is given.

Task: to conduct exploratory analysis, data preprocessing and implement linear regression in Scikit-Learn.

Information about the object: 
• full_sq – total area in sq. m, including loggias, balconies, etc.;

• life_sq – living area in sq. m, not including loggias, balconies, etc.;

• floor – floor number (for apartments); 

• max_floor – the number of floors in the building; 

• material – house material:
   panel – panel; 
   brick – brick; 
   wood – wooden; 
   mass concrete – monolithic; 
   breezeblock – blocky; 
   mass concrete plus brick – brick-monolithic; 
  
• build_year – the year the house was built; 

• num_room – number of living rooms; 

• metro_min_avto – minutes to the nearest metro station by car; 

• metro_km_avto – km to the nearest metro station by car; 

• metro_min_walk – minutes to the nearest metro station on foot; 

• metro_km_walk – km to the nearest metro station on foot; 

• mkad_km – distance to MKAD in km; 

• kremlin_km – distance to the Kremlin in km; 

• green_part_1000 – percentage of green zones within a radius of 1 km; 

• prom_part_1000 – percentage of industrial zones within a radius of 1 km; 

• office_count_1000 – the number of business centers within a radius of 1 km; 

• trc_count_1000 – the number of shopping centers within a radius of 1 km; 

• leisure_count_1000 – the number of recreation places within a radius of 1 km; 

• price_doc – the sale price of the object.        The resulting attribute (target)

Information about the area: 

• sub_area – name of the district; 

• area_m – area of the district in sq . m .; 

• green_zone_part – the proportion of green zones in the area; 

• industri_part – the share of industrial zones in the area; 

• preschool – the number of kindergartens in the district; 

• school – the number of schools in the district; 

• healthcare – the number of medical centers in the area; 

• radiation – is there any radioactive waste disposal in the area; 

• detention – is there a prison in the area; 

• young – the number of people who have not reached working age; 

• work – the number of able-bodied population; 

• elder – the population of retirement age; 

• 0_6_age – population under 6 years of age; 

• 7_14_age – the population aged from 7 to 14 years.

## Result

Significant factors:
full_sq                - total area in sq. m, including loggias, balconies, etc.;

km_score               - attractiveness score of a 1km radius around flat 

mean_price_sq_by_disc  - average price for 1 sq in this district

max_floor              - the number of floors in the building

shopping               - number of shopping centers in district

breezeblock            - whether building made out of breezeblock or not (1/0) 

mass concrete          - whether building made out of concrete or not (1/0) 

panel                  - whether building made out of panel or not (1/0)

low_prices             - whether flat is in 33 quantile of prices or not (1/0)

mid_prices             - whether flat is inbetween 33 quantile and 66 quantile of prices or not (1/0)

high_prices            - whether flat is higher than 66 quantile of prices or not (1/0)

---
The best model for this sample should be considered a polynomial of degree 2, with a staggering 88% variation and good indicators for MAO, MSE, MAPE.
---
It is worth using the usual linear regression / ridge regression, they have similar results, R^2 = 77%.
---
In extreme cases, there is a combined L1 and L2, lower error values than the subsequent ones, and a good R^2 in ~ 75%.
___

# Autor
Dmitriev Alexander - t.me/VondyB / vondy.work@gmail.com

