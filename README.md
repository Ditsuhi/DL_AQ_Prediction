# A set of deep learning algorithms for air quality prediction applications

Machine/deep learning technologies can perform predictive analyses with higher accuracy. Two machine/deep learning algorithms are introduced here to predict air quality, including grid-based (Bidirectional Convolutional Long Short-Term Memory (BiConvLSTM)) and graph-based (Attention Temporal Graph Convolutional Network (A3T-GCN)) algorithms. 

The data were obtained from Open data portal of the Madrid City Council (https://bit.ly/2TZzwEo) and the generated dataset using Arcpy library is available in the Zenodo repository (BiConvLSTM: https://doi.org/10.5281/zenodo.6076631; A3T-GCN: https://doi.org/10.5281/zenodo.7308425).

This project is licensed under the terms of the _Creative Commons Zero v1.0 Universal_ license.

## BiConvLSTM

Below is a brief description of each file included in this repository related to BiConvLSTM:

- _AirMetDataGeneration.ipynb_  combines processed air quality and meteorological data in spatiotemporal dimensions.
- _TrafficDataGeneration.ipynb_  combines processed traffic data in spatiotemporal dimensions.
- _Data\_Preprocessing.ipynb_ refers to the data pre-processing step, including implementation of the nearest neighbour interpolation, outlier detection based on the statistical summary of the dataset, and the conversion of the wind direction (converting it to categorical data (north, east, south, west, southwest, northeast, southeast, northwest) and passing through One Hot Encoder). 
- _Mutual\_Information.ipynb_ execute the Mutual information feature selection technique in order to select the most relevant features. 
- _GridSearchCV\_BlockingTimeSeriesSplit.ipynb_ refers to parameter optimisation of the proposed model performed by applying GridSearchCV with Blocking Time Series Split. 
- _Comparing\_BiConvLSTM\_ConvLSTM\_LSTM.ipynb_ develops and tests the BiConvLSTM method, and compared it with ConvLSTM and LSTM. 

## A3T-GCN

Below is a brief description of each file included in this repository related to A3T-GCN:

- _A3T-GCN_TGCN_LSTM_GRU.ipynb_ includes steps for predicting nitrogen dioxide by implementing A3T-GCN and comparing it with the results from reference methods (TGCN, LSTM and GRU).
- _Extract_Stations_Data_2019_2022.ipynb_ includes the procedure for extracting the data (raws/cells) referring only to the air quality monitoring stations' cells. 
- _Graph_Network.ipynb_ contains the procedure for constructing graph network of the air quality stations placed in the city of Madrid.
- _distanceNodes.ipynb_ includes the procedure for calculating the distance between the air quality stations placed in the city of Madrid (24 stations).
- _distanceNodes.txt_ includes the distance between the air quality stations placed in the city of Madrid (24 stations, 276 edges each edge is placed 2 times depending on the node order: origin, destination).








