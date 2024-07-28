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
Meteorology is defined as the predictive study of the state of the atmosphere, at a given locality for a given period in the future. This elaborate procedure requires information which is usually obtained from weather stations, satellite, radar as well as weather balloons. These sources give continuous records of the conditions of the immediate environment such as; temperature, humidity, pressure, wind speed and cloudiness. Meteorologists then use this data to construct the current state of weather as it is at the given period. 
</p> 
<p>
This hydrologic cycle is a most effective tool meteorologists use to predict the next day’s weather from the current day conditions by running an atmospheric model – a set of mathematical equations. Regarding Professional/Expert models, these models accommodate large amounts of data and different aspects including the pressure systems, fronts, and territory. The operation of these models allows meteorologists to forecast how the latter changes, and in what manner. 
</p>
 </div>

![Weather Change in the globe](/images/weather-wind.gif)

How is it done technically ??
======
<div style="text-align: justify"> 
<p>
The traditional basis of forecasting, Numerical Weather Prediction (NWP), has been around for decades successfully fulfilling the function of capturing atmospheric dynamics in simulation models, which are highly dependent on physics. Thereby, the technologies like these on the machine learning domain together provided a better improvement in the field of weather forecasting. METNET, the type of neural network that used smart algorithms to help the forecaster’s make a prediction of rainfall intensity with an outstanding accuracy. This blog post aims to lead you into the structure of METNET which will be done by uncovering the architecture, functions, and the future potential of the model.
</p>
 </div>



Lets see HOW is it done ?
======

NWP
------
<p>
Numerical Weather Prediction (NWP) changes the procedure of weather forecasting by using highly computational mathematical models to replicate atmosphere. NWP models are numerical weather prediction models that assimilate a large quantity of observational data from satellites, weather stations etc producing detailed forecasts. It begins with integration of current information of the atmosphere to establish first values. Next, with the help of powerful computational resources, the models describe equations for different meteorological parameters over the 3D grid of the Earth’s atmosphere and at each time step predict future states. From this method, one is able to predict from a few hours up to weeks, which is very useful for weather forecasts and climate change studies.
</p>

NWM
------
<p>
Neural Weather Modeling or NWM is the disruption of the typical method of weather prediction, Due to the use of Artificial intelligence and Neural networks to predict the state of the atmosphere. Despite drawing a lot from traditional methods of weather predictions, NWM on the other hand, uses historical climate data and data that is received from meteorological satellites or weather observation stations and other devices. All these data are processed by so called neural networks, that is the algorithms that are capable of learning the patterns and dependency in the data. This can be beneficial in the relating of future weather conditions once a model has been learned, based on the given input and correlations to observe trends. It can therefore be employed to formulate information with regard to the weather changes and issuance of warnings, as well as representation of weather reproducibly for the determination of day-to-day weather conditions.
</p>



Diving into MetNet: Forecasting by leveraging the power of DL in weather prediction
======

What is METNET
------

<div style="text-align: justify"> 
MetNet is a deep learning model that is specially designed for the short-term forecasting of the precipitation, which is between 1 to 8 hours ahead. MetNet is distinct from the customary Numerical Weather Prediction (NWP) models as it utilizes varied sources such as satellite images, radar observations and weather prediction models to identify the complex weather patterns. Its structure consists of the spatiotemporal convolutional layers and attention mechanisms that work with the data at different scales hence, it generates the high-resolution, probable forecasts. The meteorological data and the latest training methods, on the one hand, MetNet enhances the long-term weather forecasts, on the other, it becomes an important tool for use in agriculture, disaster management, urban planning and transportation.
</div>

GIF of metnet samples 1=6
======
![MetNet sample](/images/MetNet.gif)


[![METNET](https://markdown-videos-api.jorgenkh.no/url?url=https%3A%2F%2Fyoutu.be%2F-dAvqroX7ZI%3Ffeature%3Dshared)](https://youtu.be/-dAvqroX7ZI?feature=shared)



Elements OF Metnet
======

INPUT Patch 
------

Target Patch 
------

Output Layer
------

Spatial Downsampler
------

Temporal Encoder
------

Spatial Aggregator
------

Experiments 
======








Overview
------

<div style="text-align: justify"> 
MetNet is a deep learning model that is specially designed for the short-term forecasting of the precipitation, which is between 1 to 8 hours ahead. MetNet is distinct from the customary Numerical Weather Prediction (NWP) models as it utilizes varied sources such as satellite images, radar observations and weather prediction models to identify the complex weather patterns. Its structure consists of the spatiotemporal convolutional layers and attention mechanisms that work with the data at different scales hence, it generates the high-resolution, probable forecasts. The meteorological data and the latest training methods, on the one hand, MetNet enhances the long-term weather forecasts, on the other, it becomes an important tool for use in agriculture, disaster management, urban planning and transportation.
</div>

Model Description 
------
![Metnet architecture](/images/modelArchitecture.png)
![Metnet Input data](/images/MetnetInput.png)
![phy vs neural](/images/phyVsNeural.png)!
![Metnet Input data](/images/dataPatterns.png)

Why better than other model ?
------
<div style="text-align: justify"> 
Other models give to some extent the forecasts, but MetNet model is outstanding due to its singularity and high precision in the following areas:MetNet differs from the traditional model that is based on NWP models only by combining neural networks with different meteorological data. These information from this fusion helps MetNet interpret the weather conditions very accurately and detailedly to get more reliable forecasts.There is an intelligent part in the MetNet's design (convolutional layers) which helps with the analysis of huge and complex meteorological data. With the ability of following the changing complex weather operations the feature is important for real-time weather forecasting.MetNet is also contrasted to the other models which only possess a single form of definite outcome. The seasonal forecast in MetNet provides this sector with probabilistic forecast information with meaningful operating information around weather uncertainty issues. Hence, its decision making can be based on the forecast scenarios.
In conclusion, MetNet defeats all the other methods of forecasting because of the type of holistic model, a much complexer architecture with probabilistic forecasting abilities that take into account system accuracy, reliability, and feasibility.
</div>

![Metnet Input data](/images/modelComparison.png)

Experiments
------

![1st experiment](/images/modelComparison.png)
1. **Eight Hour Forecasts** Here we compare MetNet with NOAA’s current HRRR system, with a strong optical flow and with a persistence baseline using the F1 score on three precipitation rate thresholds: 0.2 mm/h, 1 mm/h and 2 mm/h. HRRR generates forecasts covering the same region as MetNet once an hour for up to 18 hours into the future at a native resolution of 3 km2. Since MetNet outputs probabilities, for each threshold we sum the probabilities along the relevant range and calibrate the corresponding F1 score on a separate validation set. MetNet outperforms HRRR substantially on the three thresholds up to a lead time of respectively 400, 440 and the full 480 minutes. MetNet is also substantially better than the optical flow method and than the persistence baseline for all lead times. The F1 score degrades for higher precipitation rate thresholds for all methods since these events become increasingly rare. Recent work using neural networks for precipitation forecasting focuses on lead times between 60 and 90 minutes with optical flow at times outperforming neural networks. MetNet is the first machine learning model to outperform HRRR and optical flow methods on a richly structured weather benchmark at such a scale and range.

![2nd experiment](/images/2ndExp.png)
2. **Ablation Experiments** Ablation experiments shed light on the importance of capturing spatial and temporal context and the importance of the various data sources in the input. The first ablation experiment reduces the spatial size of the input patch to 512 km. The very first convolutional layer in the spatial downsampling part of MetNet is removed and all else is kept exactly the same. The performance of this configuration, called MetNet-ReducedSpatial, is similar to MetNet up to 150 minutes and then it starts to become progressively worse. This indicates the importance of the large spatial context used as input as well as the ability of MetNet’s architecture to capture information contained in the original receptive field of 1024 km. This contrasts with other neural networks used for 1 hour precipitation forecasting that have a U-Net-style architecture. The receptive field of these networks at the border of the target patch is limited and likely hurts their performance and suitability for the task. The second ablation configuration is called MetNet-Reduced Temporal and reduces the temporal context of MetNet’s input features from 90 minutes prior to Tx to 30 minutes prior to Tx. This does not affect MetNet’s performance significantly and suffices to capture the advection in the input patch. In the MetNet-GOESOnly configuration, we evaluate the contribution of the MRMS data and the ability of MetNet to predict precipitation rate from just the globally available GOES-16 data. Despite starting off substantially worse, MetNet-GOESOnly’s performance approaches that of the full MetNet configuration with increasing hours of lead time suggesting that MRMS data becomes less necessary with time.




Real-Time Applications and Implications
------


1. **Disaster Management** From the angle of disaster management, sed nas continuous and progressevel high-tech level of forecasting determine an elevated level of prevention and response. The real-time forecasts of MetNet meteorological platform entitle authorities to perform fast coordination of emergency services, disasters' response and evacuation procedures in an efficient manner that is suitable to tackle situations in a prompt and proficient manner. Planning ahead in the way tactical forecast does by the fact that it determines the time to reallocate resources to areas under risks of threat, will prevent many casualties of lives and more asset losses and damages. As a result, the warning to the public at the level of commercialization and in the places that are traditionally flood-endangered leads to emergency actions like evacuation, home or property protection, etc. By developing the point at which varied agencies that comprise disaster response converge, MetNet introduces a structured and coordinated approach to managing the hazards posed by dangerous weather, this provides a platform for prevention and for handling emergency cases quickly and effectively.

2. **Urban Planning**  The prediction of accurate precipitation is essential in stormwater management tools as well as infrastructure repair in urban areas. Cities could use this approach to provide a more proactive response to urban floods and the hazards posed by its key infrastructure. By coinciding effective alerts of approaching high precipitations along with deploying temporary fences, the hiking of effective drainage systems and deduction of flood damages can be achieved. In addition, precise weather forecasting is an enabling factor for the proactive maintenance of the infrastructure systems because the service providers install siphons and remove debris from drainage systems prior to the heavy rains and thus, the risk of traffic congestions and associated floods is minimized.


3. **Agriculture** Precise forecasts of precipitation are of utmost in developing the agricultural practices in many areas. Through the provision of farmers with the possibility of creating irrigation plans which are based on the expected rainfall, resources are saved, costs are cut down and the water wastage is reduced. Besides, exact predictions help the farmers to foresee the weather conditions and hence, they can protect the crops from the adverse conditions thereby ultimately reducing the risk of damage and thus increasing the productivity. Moreover, the planning of the application of the agricultural inputs, which are fertilizers and pesticides, based on the forecasts of the weather events, gives the farmers an advantage of the better crop health, the success of treatments, and the cost-effectiveness.
   

4. **Transportation** In addition to this, anticipation helps the airlines to make the strategic flight routes decisions and execute them with proper precisions, thus allowing the airlines to soften the uncommon harsh weather like extremely heavy precipitation and strong winds. Airlines can do decision taking faster and increase safety as well with the help of alternate flight paths, which are weather patterns given that these flights will lead to fewer delays. Contrarily, the shipping majority of the industries also earn advantages by rerouting ships as there are more chances of the storm becoming negligible or a vessel getting blown away through severe rain which could be risky to the ship and the cargo. Also, with this in mind, planners will be able to carry on their scheduling of port activities to a maximum capacity as operations can easily be loaded and unloaded without any chances of adverse effects due to the climate since it will be completely put to control. The road scope information includes dynamic weather forecasts advising in advance of drivers by giving warnings or suggestions during the drives.

Future Direction
------
1. **Expanding Forecast Durations** Current MetNet capabilities outshine just in the field of providing precise forecasts up to 8 hours ahead of time. The improvement of this horizon could be of notable help. Researchers may work on modifications of the models architecture as well as data assimilating algorithms so that the acceptable length of predictions could be increased to 24 or 48 hours. The added implication will involve how certain the future is over a longer period of time and this requires more complex handling of these processes as well as data integration.

2. **Improving Computational Efficiency** Incorporating enough computing power in MetNet is essential and necessary for it to be made operational and widely utilized. Such an exercise includes the installation of different approaches targeting accelerating the model architecture and its execution procedure. Training the neural network architecture precision will be using techniques like pruning the model, quantization, and the embracement of the lightweight convolutional network that would reduce the computational time without loosing the accuracy. In addition to this, considerable attention needs to be directed towards the scalability and real-time processing functionality that happens in the real world applications. In this goal pursued by the researchers, they focus on the fact that the processes which are involved in both training and inference should run with a nett run efficiently on the standard, accessible hardware. More so, the scalability and speed are further enhanced through the parallel processing and distributed computing techniques. Therefore, solutions for energy efficiency issues become very important. Thus, software that will run the model with less energy and the hardware accelerators like GPU and TPU that can accomplish the same meaning with less computational power. 


Conclusion
------
<div style="text-align: justify"> 
Therefore, metnet is the trendsetter in weather prediction, leading to an epoch of confident and exact pronouncement of short-term detailed rainfall forecasts. Its innovation puts forward system reinforced by up-to-date deep learning algorithms and the thorough combination of different weather data sets. This represented a huge step-up in comparison with the earlier generation models. MetNet makes it to surpass conventional Numerical Weather Prediction (NWP) models and other machine learning approaches in terms of accuracy and versatility through its ability to correctly and precisely imitate a web of particular atmospheric patterns related in time and space. It has become the powerhouse of weather prediction since its probabilistic forecasts are coupled with the high ability to distinguish dangerous weather’s complexities—agriculture, disaster management, urban planning, transportation, and many others of the many endeavors on which it is being relied upon. However, MetNet is definitely on track to progress further, but different opportunities for corrections come to mind. One of the central tasks when developing AI-powered systems is supporting the systems to be adaptive in various geographical regions as well as expanding the diversity of training datasets. The partnership with leading meteorological organizations around the world will not only help stronghold, MetNet's, resilience but also fortify it across diverse climatic domains. In addition to that the computational power remains most powerful and the further research upon the perfect techniques is the necessity. MetNet not only acts as a revolutionary tool for the weather forecasting but also is a landmark of endurance and readiness in overcoming the grave risks of the unstable nature even in global scale.
</div>


References 
------
1. Sønderby, Casper & Espeholt, Lasse & Heek, Jonathan & Dehghani, Mostafa & Oliver, Avital & Salimans, Tim & Agrawal, Shreya & Hickey, Jason & Kalchbrenner, Nal. (2020). MetNet: A Neural Weather Model for Precipitation Forecasting. 
2. Hwang, Yunsung & Clark, Adam & Lakshmanan, Valliappa & Koch, Steven. (2015). Improved Nowcasts By Blending Extrapolation and Model Forecasts. Weather and Forecasting. 30. 150805113353005. 10.1175/WAF-D-15-0057.1. 
3. Shreya Agrawal, Luke Barrington, Carla Bromberg, John Burge, Cenk Gazen, and Jason Hickey. Machine learning for precipitation nowcasting from radar images.