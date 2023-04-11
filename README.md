# A set of deep learning algorithms for air quality prediction applications

Two machine/deep learning algorithms are introduced here to predict air quality, including grid-based (Bidirectional Convolutional Long Short-Term Memory) and graph-based (Attention Temporal Graph Convolutional Network) algorithms. 

## Bidirectional convolutional LSTM 

Nitrogen dioxide is one of the pollutants with the most significant health effects. Advanced information on its concentration in the air can help to monitor and control further consequences more effectively, while also making it easier to apply preventive and mitigating measures. Machine learning technologies with available methods and capabilities, combined with the geospatial dimension, can perform predictive analyses with higher accuracy and, as a result, can serve as a supportive tool for productive management. One of the most advanced machine learning algorithms, Bidirectional convolutional LSTM, is being used in ongoing work to predict the concentration of nitrogen dioxide. The model has been validated to perform more accurate spatiotemporal analysis based on the integration of temporal and geospatial factors. The analysis was carried out according to two scenarios developed on the basis of selected features using data from the city of Madrid for the periods January-June 2019 and January-June 2020. Evaluation of the model's performance was conducted utilising the Root Mean Square Error and the Mean Absolute Error which emphasises the superiority of the proposed model over the reference models. In addition, the significance of a feature selection technique providing improved accuracy was underlined. In terms of execution time, due to the complexity of the Bidirectional convolutional LSTM architecture, convergence and generalisation of the data took longer, resulting in the superiority of the reference models.


The data were obtained from Open data portal of the Madrid City Council (https://bit.ly/2TZzwEo) and the generated dataset using Arcpy library is available in the Zenodo repository (DOI:https://doi.org/10.5281/zenodo.6076631).

Below is a brief description of each file included in this repository:

- _AirMetDataGeneration.ipynb_  combines processed air quality and meteorological data in spatiotemporal dimensions.
- _TrafficDataGeneration.ipynb_  combines processed traffic data in spatiotemporal dimensions.
- _Data\_Preprocessing.ipynb_ refers to the data pre-processing step, including implementation of the nearest neighbour interpolation, outlier detection based on the statistical summary of the dataset, and the conversion of the wind direction (converting it to categorical data (north, east, south, west, southwest, northeast, southeast, northwest) and passing through One Hot Encoder). 
- _Mutual\_Information.ipynb_ execute the Mutual information feature selection technique in order to select the most relevant features. 
- _GridSearchCV\_BlockingTimeSeriesSplit.ipynb_ refers to parameter optimisation of the proposed model performed by applying GridSearchCV with Blocking Time Series Split. 
- _Comparing\_BiConvLSTM\_ConvLSTM\_LSTM.ipynb_ develops and tests the BiConvLSTM method, and compared it with ConvLSTM and LSTM. 

## Attention Temporal Graph Convolutional Network

Air quality monitoring, modelling and forecasting are considered pressing and challenging topics for citizens and decision-makers, including the government. The tools used to achieve the above goals vary depending on the opportunities provided by technological development. Much attention is currently being paid to machine learning and deep learning methods, which, compared to domain knowledge methods, often perform better in terms of capturing, computing and processing multidimensional information and complex dependencies. The technique introduced in this work is an Attention Temporal Graph Convolutional Network based on a combination of Attention, a Gated Recurrent Unit and a Graph Convolutional Network. In the framework of the current study, it is initially suggested to use the presented approach in the domain of air quality prediction. The proposed method was tested using air quality, meteorological and traffic data obtained from the city of Madrid for the periods January-June 2019 and January-June 2022. The evaluation metrics, including Root Mean Square Error, Mean Absolute Error and Pearson Correlation Coefficient, confirmed the proposed model's advantages compared with the reference models (Temporal Graph Convolutional Network, Long Short-Term Memory and Gated Recurrent Unit).


The purpose of each file included in this repository is briefly described below:

- _A3T-GCN_TGCN_LSTM_GRU.ipynb_ includes steps for predicting nitrogen dioxide by implementing A3T-GCN and comparing it with the results from reference methods (TGCN, LSTM and GRU).
- _Extract_Stations_Data_2019_2022.ipynb_ includes the procedure for extracting the data (raws/cells) referring only to the air quality monitoring stations' cells. 
- _Graph_Network.ipynb_ contains the procedure for constructing graph network of the air quality stations placed in the city of Madrid.
- _distanceNodes.ipynb_ includes the procedure for calculating the distance between the air quality stations placed in the city of Madrid (24 stations).
- _distanceNodes.txt_ includes the distance between the air quality stations placed in the city of Madrid (24 stations, 276 edges each edge is placed 2 times depending on the node order: origin, destination).


The datasets can be found at the following link: https://doi.org/10.5281/zenodo.7308425.






