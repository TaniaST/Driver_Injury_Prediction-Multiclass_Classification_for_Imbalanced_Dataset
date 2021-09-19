## Driver's Injury Prediction - Multiclass Classification Models
### Goal
The purpose of the study is to predict driver’s injury level in a car crash using Random Forest, Support Vector Machines, K-Nearest Neighbours, XGBoost and CNN models. The data used for the analysis are the records of bodily injury accidents occurred between two cars in Metropolitan France in 2005-2017. The outcome variable is severity of the accident 
represented by four levels of injury: “no injury”, “light injury”, “hospitalised” and “killed”. 


### Data Description
The dataset we have analysed contains 254887 observations of accidents between two cars, occurred in metropolitan France between 2005 and 2017, the variables in which can be grouped into four categories:

• Characteristics (year, month, day and hour of accident, type of collision, department and commune codes, postal address, metropolitan France vs. DOM-TOM territories flag, latitude,
longitude, lighting conditions, whether the accident took place in built-up area, junction type, atmospheric conditions etc);

• Places (road type, traffic type, number of lanes, road slope, shape of the road segment, width of the lane, road surface state, infrastructure details, the exact place of the accident, proximity of
school, road name, presence of special lanes for bicycles, the closest milestone number, width of the median strip);

• Vehicles (fixed obstacle hit during the accident, moving obstacle hit during the accident, initial place of shock, direction of the traffic flow, vehicle category, main movement before the accident,
number of people in public transport);

• People (gender, year of birth, reason for journey, type of security equipment, place of the victim in the vehicle, victim category, localisation of the pedestrian, action of the pedestrian, flag
indicating if the pedestrian was alone, severity of victim’s injury).

### Code and Results
The **"Summary"** file briefly summarises the main findings of the study.

The **"project_EDA"** file shows the code and results of the exploratory data analysis.

The **"Models"** file shows the code and results for Random Forest, Support Vector Machines, K-Nearest Neighbours and XGBoost models

The **"CNN Models"** file shows the code and results for two different CNN models: one designed directly for the four-classes outcome and another created using transfer learning technique.

### How to run the code
The code is to be run in the following order:
1. take "data" zip folder and copy to your local directory
2. extract files contained in "data" zip folder
3. take "subset" csv file and put in your local directory
4. open "project_preprocessing_data", change the importing and output directories to your own and run the code, it will import and preprocess dataset and then export the pre-processed dataset to your directory. Pre-processed dataset is also directly available in "subset_2class_agg" file.
5. open "project_EDA" file, change importing directory to your own and run the code, it will show Exploratory Data Analysis results
6. open "Models" file, change importing directory to your own and run the code, it will show Random Forest, SVM, KNN and XGBoost models results
7. open "CNN Models" file, choose your importing directory and run the code, it will show CNN models results
