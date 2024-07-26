# Harnessing Citizen Science to Enhance Land Surface Temperature Prediction

## Project Overview
This research project, conducted by 2024 NASA SEES Interns (Kevin Diaz, Kandyce Diep, Suhani Dondapati, Maako Fangajei, Anna Felten, Kei Fry, Conor Furey, Aaren George), utilizes citizen science to create a machine learning model trained to predict land surface temperatures (LSTs). This research question was addressed using GLOBE Observer down photos in conjunction with Landsat-8 data used to train two machine learning models: Random Forest and XGBoost. For both Random Forest and XGBoost, we trained the model on three separate datasets: one with coordinate data, one with coordinate & GLOBE data, and one comprehensive model with coordinate, GLOBE, and CEO data. We evaluated models with three statistical metrics: R^2, RMSE, and MAE. The hypothesis was that incorporating vegetation data and Collect Earth Online data into the machine learning models with coordinate data would provide greater accuracy for predicting land surface temperatures.

## Description of Repository Files

There are two Google Colab notebooks included in the Training Notebooks directory.

* V_EX_Group_2_ML_Notebook_Random_Forest.ipynb
    * contains all necessary code for processing data and training three separate Random Forest models.
* V_EX_Group_2_ML_Notebook_XGBoost.ipynb
    * contains all necessary code for processing data and training three separate XGBoost models.

The data used for training the models is included in the Training Data directory:
* model1_dataset.csv
	* contains only latitude and longitude data, along with an image ID that corresponds to an image ID from the GLOBE Observer Down Photos directory
* model2_dataset.csv
	* contains coordinate data (latitude and longitude), along with citizen-labeled data from Zooniverse for GLOBE Observer photos
* model3_dataset.csv
	* contains coordinate data, citizen-labeled data from Zooniverse, and labeled satellite data from Collect Earth Online associated with each image's location

Additionally, the GitHub contains raw data files used to create processed data:
* GLOBE Observer Down Photos
    * Contains all 958 raw "down photos" from the SEES 2024 intern team, later uploaded to Zooniverse for labeling
* Raw Zooniverse data
	* Contains the raw labeled image data from Zooniverse
* Raw Collect Earth Online Data
    * Contains the raw labeled satellite data from Collect Earth Online for 47 separate areas of interest, separated into 5 files (CEO_1.csv, CEO_2.csv, CEO_3.csv, CEO_4.csv, and CEO_5.csv) due to the large size of the dataset

## Steps to Reproduce Results
1. Download all files in the Training Data folder (model1_dataset.csv, model2_dataset.csv, and model3_dataset.csv). Upload to Google Drive.
2. Run the Random Forest notebook to obtain Random Forest results. You may need to change the path to each dataset in your code. 
3. Run the XGBoost notebook to obtain XGBoost results. You may need to change the path to each dataset in your code. 

## Citations and Acknowledgments

The authors would like to acknowledge the support of the 2024 Earth System Explorers (ESE) Team, NASA Science Mentors, and ESE peer mentors. NASA STEM Enhancement in the Earth Sciences (SEES) Virtual High School Internship program. The NASA Earth Science Education Collaborative leads Earth Explorers through an award to the Institute for Global Environmental Strategies, Arlington, VA (NASA Award NNX6AE28A). The SEES High School Summer Intern Program is led by the Texas Space Grant Consortium at the University of Texas at Austin (NASA Award NNX16AB89A0).

Specifically, the research project was heavily influenced by the guidance of our mentors: Andrew Clark, Russanne Low, Peder Nelson, Cassie Soeffing, Ollie Snow, and Riya Tyagi. Rusty provided knowledge about the principles of citizen science, allowing us to cross-validate our data to ensure our findings were reliable and scientifically sound. Peder introduced us to GIS software such as Zooniverse and Collect Earth Online, improving our data labeling and categorization. Cassie advised us on effectively communicating our research goals. Andrew introduced us to ORCiD and open data concepts. Riya and Ollie served as our peer mentors. Riya provided technical advice on using AI models for the project, while Ollie helped with image labeling details on Collect Earth Online. Their combined efforts made this project possible. We extend our thanks to each of them for their contributions.
