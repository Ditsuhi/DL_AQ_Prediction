# Bidirectional convolutional LSTM for the prediction of nitrogen dioxide in the city of Madrid

Nitrogen dioxide is one of the pollutants with the most significant health effects. Advanced information on its concentration in the air can help to monitor and control further consequences more effectively, while also making it easier to apply preventive and mitigating measures. Machine learning technologies with available methods and capabilities, combined with the geospatial dimension, can perform predictive analyses with higher accuracy and, as a result, can serve as a supportive tool for productive management. One of the most advanced machine learning algorithms, Bidirectional convolutional LSTM, is being used in ongoing work to predict the concentration of nitrogen dioxide. The model has been validated to perform more accurate spatiotemporal analysis based on the integration of temporal and geospatial factors. The analysis was carried out according to two scenarios developed on the basis of selected features using data from the city of Madrid for the periods January-June 2019 and January-June 2020. Evaluation of the model's performance was conducted utilising the Root Mean Square Error and the Mean Absolute Error which emphasises the superiority of the proposed model over the reference models. In addition, the significance of a feature selection technique providing improved accuracy was underlined. In terms of execution time, due to the complexity of the Bidirectional convolutional LSTM architecture, convergence and generalisation of the data took longer, resulting in the superiority of the reference models.


The data were obtained from Open data portal of the Madrid City Council (https://bit.ly/2TZzwEo) and the generated dataset using Arcpy library is available in the Zenodo repository (DOI:https://doi.org/10.5281/zenodo.6076631).

Below is a brief description of each file included in this repository:

- _AirMetDataGeneration.ipynb_  combines processed air quality and meteorological data in spatiotemporal dimensions.
- _TrafficDataGeneration.ipynb_  combines processed traffic data in spatiotemporal dimensions.
- _Data\_Preprocessing.ipynb_ refers to the data pre-processing step, including implementation of the nearest neighbour interpolation, outlier detection based on the statistical summary of the dataset, and the conversion of the wind direction (converting it to categorical data (north, east, south, west, southwest, northeast, southeast, northwest) and passing through One Hot Encoder). 
- _Mutual\_Information.ipynb_ execute the Mutual information feature selection technique in order to select the most relevant features. 
- _GridSearchCV\_BlockingTimeSeriesSplit.ipynb_ refers to parameter optimisation of the proposed model performed by applying GridSearchCV with Blocking Time Series Split. 
- _Comparing\_BiConvLSTM\_ConvLSTM\_LSTM.ipynb_ develops and tests the BiConvLSTM method, and compared it with ConvLSTM and LSTM. 






