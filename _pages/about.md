---
permalink: /
title: "MetNet: A Neural Weather Model for Precipitation Forecasting"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
 

What is Weather Forecasting ? 
======

<div style="text-align: justify"> 
<p>
Forecasting is defined as the predictive study of the state of the atmosphere, at a given locality for a given period in the future. This elaborate procedure requires information which is usually obtained from weather stations, satellite, radar as well as weather balloons. These sources give continuous records of the conditions of the immediate environment such as - temperature, humidity, pressure, wind speed and cloudiness. Meteorologists then use this data to construct the current state of weather as it is at the given period. 
</p> 
<p>
This hydrologic cycle is a most effective tool meteorologists use to predict the next day’s weather from the current day conditions by running an atmospheric model – a set of mathematical equations. Regarding professional models, these models accommodate large amounts of data and different aspects including the pressure systems, fronts and territory. The operation of these models allows meteorologists to forecast how the weather changes and in what manner. 
</p>
 </div>

![Weather Change in the globe](/images/weather-wind.gif)

How is it done technically ?
======
<div style="text-align: justify"> 
<p>
The traditional basis of forecasting, Numerical Weather Prediction (NWP), has been around for decades successfully fulfilling the function of capturing atmospheric dynamics in simulation models, which are highly dependent on physics. Thereby, the technologies like these on the machine learning domain together provided a better improvement in the field of weather forecasting. METNET, the type of neural network that used smart algorithms to help the forecaster’s make a prediction of rainfall intensity with an outstanding accuracy. This blog post aims to lead you into the structure of METNET which will be done by uncovering the architecture, functions, and the future potential of the model.
</p>
 </div>



Lets see HOW is it done ?
======

![phy vs neural](/images/phyVsNeural.png "Image: 'Sunset Over the Mountains,' by John Doe, from Unsplash, 2023")

<p align="right">
[1]
</p>

NWP
------
<p style="text-align: justify;">
Numerical Weather Prediction (NWP) changes the procedure of weather forecasting by using highly computational mathematical models to replicate atmosphere. NWP models are numerical weather prediction models that assimilate a large quantity of observational data from satellites, weather stations etc producing detailed forecasts. It begins with integration of current information of the atmosphere to establish first values. Next, with the help of powerful computational resources, the models describe equations for different meteorological parameters over the 3D grid of the earth’s atmosphere and at each time step predict future states. From this method, one is able to predict from a few hours up to weeks, which is very useful for weather forecasts and climate change studies.
</p>

NWM
------
<p style="text-align: justify;">
Neural Weather Modeling or NWM is the disruption of the typical method of weather prediction, Due to the use of Artificial intelligence and Neural networks to predict the state of the atmosphere. Despite drawing a lot from traditional methods of weather predictions, NWM on the other hand, uses historical climate data and data that is received from meteorological satellites or weather observation stations and other devices. All these data are processed by so called neural networks, that is the algorithms that are capable of learning the patterns and dependency in the data. This can be beneficial in the relating of future weather conditions once a model has been learned, based on the given input and correlations to observe trends. It can therefore be employed to formulate information with regard to the weather changes and issuance of warnings, as well as representation of weather reproducibly for the determination of day-to-day weather conditions.
</p>

NWP vs NWM
------
![MetNet sample](/images/comparison.png)


Diving into MetNet: Forecasting by leveraging the power of DL in weather prediction
======

What is METNET
------

<div style="text-align: justify"> 
<p align="justify">
MetNet is a deep learning model that is specially designed for the short-term forecasting of the precipitation, which is between 1 to 8 hours ahead. MetNet is distinct from the customary Numerical Weather Prediction (NWP) models as it utilizes varied sources such as satellite images, radar observations and weather prediction models to identify the complex weather patterns. Its structure consists of the spatiotemporal convolutional layers and attention mechanisms that work with the data at different scales hence, it generates the high-resolution, probable forecasts. The meteorological data and the latest training methods, on the one hand, MetNet enhances the long-term weather forecasts, on the other, it becomes an important tool for use in agriculture, disaster management, urban planning and transportation.
</p>
<p align="justify">
Below you can see some samples from the comparison of Metnet(NWM), Ground Truth and HRRR (NWP) model respectively.
</p>
</div>

![MetNet sample](/images/MetNet.gif)

<p>
<div style="text-align: center;">
    <iframe width="320" height="315" src="https://www.youtube.com/embed/-dAvqroX7ZI" frameborder="0" allowfullscreen></iframe>
</div>
</p>
<p align="right">
[4]
</p>

Elements OF Metnet
======
![Metnet architecture](/images/modelArchitecture.png) 
<p align="right">
[1]
</p>

INPUT Patch 
------

<img src="/images/inp-1.png" alt="Image 1" style="width:45%; display:inline-block; margin-right:10px;">
<img src="/images/inp-2.png" alt="Image 2" style="width:45%; display:inline-block;">
<p style="text-align: justify;" >

<p align="right">
[1]
</p>
MetNet is advanced weather forecast model with a particular focus of what suitable for analyzing an immense amount of data so as to determine the future state of the weather. It analyzes a four-dimensional set of information that contains time, area, and different kinds of measurements. More specifically, MetNet studies the values of 15-minutes intervals in 90 minutes preceding the predicted time. This proposition identifies a relatively big 1024 by 1024 kilometer area of the continental United States. The model uses one radar image for precipitation, 16 different spectral bands from GOES-16 satellite and general information about each location's longitude, latitude, and altitude. Furthermore, it contains the temporal attributes which include the hour, day, and the month of the prediction time distributed in the whole grid. Thus, including all this detailed data in the analysis, MetNet can provide very accurate weather predictions.
</p>

![Metnet Input data](/images/MetnetInput.png)
<p align="right">
[1]
</p>

Target Patch 
------

<p align="center">
  <img src="/images/target.png" alt="2nd experiment" style="max-width:100%; height:auto;">
<p align="right">
[1]
</p>
</p>




<p style="text-align: justify;" >
If MetNet has to predict the weather up to 8 hours in advance, it examines a huge area of 1024 x 1024 kilometers so as to register every activity concerning the weather in the vicinity of the targeted area. It primarily zeroes in on the 64 x 64 km square in the middle, but encases it in a 480-kilometer ring that helps it monitor any shift in the weather the location may be experiencing, ensuring it has enough information for accurate prediction.
</p>


Output Layer
------
<p align="center">
  <img src="/images/output.png" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>
<p align="right">
[1]
</p>

<p style="text-align: justify;" >
MetNet’s output is a forecast covering 512 categories to show varying intensity of rainfall, which ranges from a particular level to another. These categories impound the rainfall rate ranging from 0 mm/h to 102. 4 mm/h; they can be classified as low-intensity rain with a rate determined according to the following scale: 0. 2 mm/h intervals. Any rate of rainfall more than 102. 4 mm/h is and belongs to the last group of the lower maximum intensity rate. In order to see the probability of some given range of rainfall or rates above some barrier one sums up the probabilities of the corresponding categories.
</p>

Spatial Downsampler
------

<p align="center">
  <img src="/images/down.png" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>
<p align="right">
[1]
</p>
<p style="text-align: justify;" >
 Due to the problem of memory and computing resources, MetNet performs several convolution and pooling to shrink the input data set in order to capture all essential details. Every time slice of the input is resized and is passed through a 3x3 convolution layers having 160 filters followed by 3 x 3 convolution layers having 256 filters and 2 x 2 max pooling reducing its size in each step. The final outcome of this process is that the size of a time slice has been reduced to 64 x 64 with 256 channel values for the data to enable further processing by the chosen model.
</p>

Temporal Encoder
------

<p align="center">
  <img src="/images/temp.png" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>
<p align="right">
[1]
</p>

<p style="text-align: justify;" >
The second part of MetNet takes care of processing the input data over time, in which the contracted time slices are passed to a recurrent neural network (RNN) sequentially in time. For instance, it applies a ConvLSTM with a 3 x 3 receptive filed and 384 channels to learn temporal features. This increases the influence of the recent data slices, and the final output – 64 x 64 tensor with the channel number of 384 – contains information about the input patch both by spatial and temporal dimensions.
</p>



Spatial Aggregator
------

<p align="center">
  <img src="/images/aggregator.png" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>
<p align="right">
[1]
</p>
<p style="text-align: justify;" >
To ensure MetNet covers the entire spatial context of the input patch, the third part uses eight axial self-attention blocks, with four operating along the width and four along the height. Each block has 2048 channels and 16 attention heads, effectively capturing the full context with fewer computations than traditional self-attention. This approach allows MetNet to reach the global context in just two blocks instead of the 32 blocks required by standard 3x3 convolutions, resulting in a model with 225 million parameters.
</p>




Why better than other model ?
------
<div style="text-align: justify"> 
<p>
Other models give to some extent the forecasts, but MetNet model is outstanding due to its singularity and high precision in the following areas:MetNet differs from the traditional model that is based on NWP models only by combining neural networks with different meteorological data. These information from this fusion helps MetNet interpret the weather conditions very accurately and detailedly to get more reliable forecasts.There is an intelligent part in the MetNet's design (convolutional layers) which helps with the analysis of huge and complex meteorological data. With the ability of following the changing complex weather operations the feature is important for real-time weather forecasting.MetNet is also contrasted to the other models which only possess a single form of definite outcome. The seasonal forecast in MetNet provides this sector with probabilistic forecast information with meaningful operating information around weather uncertainty issues. Hence, its decision making can be based on the forecast scenarios.
</p>
<p>
In conclusion, MetNet defeats all the other methods of forecasting because of the type of holistic model, a much complexer architecture with probabilistic forecasting abilities that take into account system accuracy, reliability, and feasibility.
</p>
</div>

What is Special in METNET ?
======

<p align="justify">
Regarding the abilities of <strong>MetNet</strong>, it has ability to handle large data easily and <strong>axial attention</strong> helps in the improvement of weather forecasting by understanding massive data like high-resolution satellite images. Imagine trying to understand a big map: In the case of the standard self-attention, it is as if one wants to match every location on the map with every other point simultaneously, and this does not work efficiently, and quickly gets overwhelming. Axial attention makes this easier by first attending to one axis at a time in a way that, for instance, one is looking at the row elements first and then the column ones. This is much <strong>quicker</strong> and requires <strong>less memory</strong> which enables MetNet to quickly transverse large maps of weather data and make forecast that do not become overwhelmed by the amount of data.
</p>
<p align="center">
  <img src="/images/axial.png" alt="axial" style="max-width:100%; height:auto;">
</p>
<p align="right">
[5]
</p>


Experiments 
======


**Eight Hour Forecasts** 

![1st experiment](/images/modelComparison.png)

<p align="right">
[1]
</p>

<p style="text-align: justify">Here we compare MetNet with NOAA’s current HRRR system, with a strong optical flow and with a persistence baseline using the F1 score on three precipitation rate thresholds: 0.2 mm/h, 1 mm/h and 2 mm/h. HRRR generates forecasts covering the same region as MetNet once an hour for up to 18 hours into the future at a native resolution of 3 km2. Since MetNet outputs probabilities, for each threshold we sum the probabilities along the relevant range and calibrate the corresponding F1 score on a separate validation set. MetNet outperforms HRRR substantially on the three thresholds up to a lead time of respectively 400, 440 and the full 480 minutes. </p> 
<p>MetNet is also substantially better than the optical flow method and than the persistence baseline for all lead times. The F1 score degrades for higher precipitation rate thresholds for all methods since these events become increasingly rare. Recent work using neural networks for precipitation forecasting focuses on lead times between 60 and 90 minutes with optical flow at times outperforming neural networks. MetNet is the first machine learning model to outperform HRRR and optical flow methods on a richly structured weather benchmark at such a scale and range.
</p>



**Ablation Experiments** 

![2nd experiment](/images/2ndExp.png)

<p align="right">
[1]
</p>

<p style="text-align: justify"> Ablation experiments shed light on the importance of capturing spatial and temporal context and the importance of the various data sources in the input. The first ablation experiment reduces the spatial size of the input patch to 512 km. The very first convolutional layer in the spatial downsampling part of MetNet is removed and all else is kept exactly the same. The performance of this configuration, called MetNet-ReducedSpatial, is similar to MetNet up to 150 minutes and then it starts to become progressively worse. This indicates the importance of the large spatial context used as input as well as the ability of MetNet’s architecture to capture information contained in the original receptive field of 1024 km. This contrasts with other neural networks used for 1 hour precipitation forecasting that have a U-Net-style architecture. The receptive field of these networks at the border of the target patch is limited and likely hurts their performance and suitability for the task. 
</p>
<p style="text-align: justify">The second ablation configuration is called MetNet-Reduced Temporal and reduces the temporal context of MetNet’s input features from 90 minutes prior to Tx to 30 minutes prior to Tx. This does not affect MetNet’s performance significantly and suffices to capture the advection in the input patch. In the MetNet-GOESOnly configuration, we evaluate the contribution of the MRMS data and the ability of MetNet to predict precipitation rate from just the globally available GOES-16 data. Despite starting off substantially worse, MetNet-GOESOnly’s performance approaches that of the full MetNet configuration with increasing hours of lead time suggesting that MRMS data becomes less necessary with time.
</p>



Real-Time Applications and Implications:
======

**Disaster Management**  

<p align="center">
  <img src="/images/disaster.jpeg" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>

*Image: Disaster Management with help of DL* [Microsoft Image Designer](https://designer.microsoft.com/) 

<p style="text-align: justify;">

From the angle of disaster management, sed nas continuous and progressevel high-tech level of forecasting determine an elevated level of prevention and response. The real-time forecasts of MetNet meteorological platform entitle authorities to perform fast coordination of emergency services, disasters' response and evacuation procedures in an efficient manner that is suitable to tackle situations in a prompt and proficient manner. Planning ahead in the way tactical forecast does by the fact that it determines the time to reallocate resources to areas under risks of threat, will prevent many casualties of lives and more asset losses and damages. As a result, the warning to the public at the level of commercialization and in the places that are traditionally flood-endangered leads to emergency actions like evacuation, home or property protection, etc. 
  </p>

<p style="text-align: justify;">
By developing the point at which varied agencies that comprise disaster response converge, MetNet introduces a structured and coordinated approach to managing the hazards posed by dangerous weather, this provides a platform for prevention and for handling emergency cases quickly and effectively.
</p>


**Urban Planning**  

<p align="center">
  <img src="/images/urban.jpeg" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>

*Image: Urban Planning with help of DL* [Microsoft Image Designer](https://designer.microsoft.com/) 

<p style="text-align: justify;">
The prediction of accurate precipitation is essential in stormwater management tools as well as infrastructure repair in urban areas. Cities could use this approach to provide a more proactive response to urban floods and the hazards posed by its key infrastructure. By coinciding effective alerts of approaching high precipitations along with deploying temporary fences, the hiking of effective drainage systems and deduction of flood damages can be achieved. In addition, precise weather forecasting is an enabling factor for the proactive maintenance of the infrastructure systems because the service providers install siphons and remove debris from drainage systems prior to the heavy rains and thus, the risk of traffic congestions and associated floods is minimized.

</p>


**Agriculture** 

<p align="center" style="position: relative; display: inline-block;" >
  <img src="/images/agri.jpeg" alt="2nd experiment" style="max-width:100%; height:auto;">
 <span style="position: absolute; bottom: 0; right: 0; margin: 5px;">[1]</span>
</p>
*Image: Agriculture with help of DL* [Microsoft Image Designer](https://designer.microsoft.com/) 

<p style="text-align: justify;">
Precise forecasts of precipitation are of utmost in developing the agricultural practices in many areas. Through the provision of farmers with the possibility of creating irrigation plans which are based on the expected rainfall, resources are saved, costs are cut down and the water wastage is reduced. Besides, exact predictions help the farmers to foresee the weather conditions and hence, they can protect the crops from the adverse conditions thereby ultimately reducing the risk of damage and thus increasing the productivity. Moreover, the planning of the application of the agricultural inputs, which are fertilizers and pesticides, based on the forecasts of the weather events, gives the farmers an advantage of the better crop health, the success of treatments, and the cost-effectiveness.
</p>

**Transportation** 

<p align="center">
  <img src="/images/transport.jpeg" alt="2nd experiment" style="max-width:100%; height:auto;">
</p>

*Image: Tranpotation with help of DL* [Microsoft Image Designer](https://designer.microsoft.com/) 

<p style="text-align: justify;">
In addition to this, anticipation helps the airlines to make the strategic flight routes decisions and execute them with proper precisions, thus allowing the airlines to soften the uncommon harsh weather like extremely heavy precipitation and strong winds. Airlines can do decision taking faster and increase safety as well with the help of alternate flight paths, which are weather patterns given that these flights will lead to fewer delays. Contrarily, the shipping majority of the industries also earn advantages by rerouting ships as there are more chances of the storm becoming negligible or a vessel getting blown away through severe rain which could be risky to the ship and the cargo. Also, with this in mind, planners will be able to carry on their scheduling of port activities to a maximum capacity as operations can easily be loaded and unloaded without any chances of adverse effects due to the climate since it will be completely put to control. The road scope information includes dynamic weather forecasts advising in advance of drivers by giving warnings or suggestions during the drives.
</p> 

Future Direction
======



**Expanding Forecast Durations** 

<p style="text-align: justify;">
Current MetNet capabilities outshine just in the field of providing precise forecasts up to 8 hours ahead of time. The improvement of this horizon could be of notable help. Researchers may work on modifications of the models architecture as well as data assimilating algorithms so that the acceptable length of predictions could be increased to 24 or 48 hours. The added implication will involve how certain the future is over a longer period of time and this requires more complex handling of these processes as well as data integration.
</p>


**Improving Computational Efficiency** 
<p style="text-align: justify;">
Incorporating enough computing power in MetNet is essential and necessary for it to be made operational and widely utilized. Such an exercise includes the installation of different approaches targeting accelerating the model architecture and its execution procedure. Training the neural network architecture precision will be using techniques like pruning the model, quantization, and the embracement of the lightweight convolutional network that would reduce the computational time without loosing the accuracy. In addition to this, considerable attention needs to be directed towards the scalability and real-time processing functionality that happens in the real world applications. In this goal pursued by the researchers, they focus on the fact that the processes which are involved in both training and inference should run with a nett run efficiently on the standard, accessible hardware. More so, the scalability and speed are further enhanced through the parallel processing and distributed computing techniques. Therefore, solutions for energy efficiency issues become very important. Thus, software that will run the model with less energy and the hardware accelerators like GPU and TPU that can accomplish the same meaning with less computational power. 
</p>


Conclusion
======


<p style="text-align: justify;">
Therefore, metnet is the trendsetter in weather prediction, leading to an epoch of confident and exact pronouncement of short-term detailed rainfall forecasts. Its innovation puts forward system reinforced by up-to-date deep learning algorithms and the thorough combination of different weather data sets. This represented a huge step-up in comparison with the earlier generation models. 
</p>
<p style="text-align: justify;">
MetNet makes it to surpass conventional Numerical Weather Prediction (NWP) models and other machine learning approaches in terms of accuracy and versatility through its ability to correctly and precisely imitate a web of particular atmospheric patterns related in time and space. It has become the powerhouse of weather prediction since its probabilistic forecasts are coupled with the high ability to distinguish dangerous weather’s complexities—agriculture, disaster management, urban planning, transportation, and many others of the many endeavors on which it is being relied upon. However, MetNet is definitely on track to progress further, but different opportunities for corrections come to mind. One of the central tasks when developing AI-powered systems is supporting the systems to be adaptive in various geographical regions as well as expanding the diversity of training datasets. 
</p>
<p style="text-align: justify;">
The partnership with leading meteorological organizations around the world will not only help stronghold, MetNet's, resilience but also fortify it across diverse climatic domains. In addition to that the computational power remains most powerful and the further research upon the perfect techniques is the necessity. MetNet not only acts as a revolutionary tool for the weather forecasting but also is a landmark of endurance and readiness in overcoming the grave risks of the unstable nature even in global scale.
</p>





References 
======

1. Sønderby, Casper & Espeholt, Lasse & Heek, Jonathan & Dehghani, Mostafa & Oliver, Avital & Salimans, Tim & Agrawal, Shreya & Hickey, Jason & Kalchbrenner, Nal. (2020). MetNet: A Neural Weather Model for Precipitation Forecasting. 
2. Hwang, Yunsung & Clark, Adam & Lakshmanan, Valliappa & Koch, Steven. (2015). Improved Nowcasts By Blending Extrapolation and Model Forecasts. Weather and Forecasting. 30. 150805113353005. 10.1175/WAF-D-15-0057.1. 
3. Shreya Agrawal, Luke Barrington, Carla Bromberg, John Burge, Cenk Gazen, and Jason Hickey. Machine learning for precipitation nowcasting from radar images.
4. Nal Kalchbrenner, Neural Weather Model MetNet: Samples - https://www.youtube.com/watch?v=-dAvqroX7ZI
5. Ho, Jonathan & Kalchbrenner, Nal & Weißenborn, Dirk & Salimans, Tim. (2019). Axial Attention in Multidimensional Transformers. 


