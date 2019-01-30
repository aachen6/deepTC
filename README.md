# DeepTC

Tropical Cyclones, hereafter referred to as TCs, are severe weather system originated over warm tropical ocean. They are known as hurricanes in the Atlantic and Northeast Pacific, cyclones in the South Pacific and Indian Ocean, and typhoons in the Northwest Pacific. TCs typically move from east to west due to the tropical trade winds near the equator where the TCs originate, and curve into higher latitude as a result of the Coriolis force and steering winds at higher elevation. Many TCs made direct landfall, which caused significant threat to life and property. Although the westerly winds prevail at higher altitude may steer the storm back to the east into the ocean and some of them may be weakened to a tropical storm or become extratropical, TCs can still produce hurricane-force winds and high storm surge along the coast even remained offshore. For the TC warning and disaster management, the prediction of the intensity as well as the track of the TCs is very important for the local authorities in their decision making regarding the time and location of evacuation to reduce the potential damage due to the TCs.

The Dvorak technique is the most widely used methodology that estimates TC intensity, which correlates TC intensities to various cloud patterns of central and banding features in the infrared images from geostationary satellites. This technique suffers from subjectivity of the storm center selection and scene type determination procedures. Advanced Dvorak Technique for the estimation of TC intensity have been developed to reduce such subjectivity by using computer-based algorithms for recognizing cloud features, which is currently used in the NOAA operational model for estimation of storm intensity. However, such heuristic rule approach requires regional nuances and adjustment and always suffers from heuristic exception of rules that are not predefined. 

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/DvorakCDP1973.png/1280px-DvorakCDP1973.png" width="400"/>*Image credit: Wikipedia*

The prediction of TC track relies on global numerical weather models that solve the mathematical equations governing the behavior of the atmosphere at every point on the globel. According to [this article](https://www.wunderground.com/hurricane/models.asp) by Dr. Jeff Masters, Director of Meteorology from NOAA, the top six dynamical models for the TS track and intensity forecast are 

- ECMWF: The European Center for Medium-Range Weather Forecasting (ECMWF) model is the premier global model in the world for medium range weather forecasting in the mid-latitudes;
 
- GFS: The Global Forecast System model run by the NWS;
 
- GFDL: The NWS/Geophysical Fluid Dynamics Laboratory model. The GFDL and HWRF models are the only models that provide specific intensity forecasts of hurricanes;
 
- UKMET: The United Kingdom Met Office model;
 
- HWRF: The NWS/Hurricane Weather Research Model, which is a non-hydrostatic a coupled ocean-atmosphere model, will utilize highly advanced physics of the atmosphere, ocean and waves in one prediction system, providing unparalleled understanding of the science of tropical cyclone evolution;
 
- NOGAPS: The U.S. Navy's Navy Operational Global Prediction Center System. 
 
These models take several hours to run on the world's most advanced supercomputers and produce results with high variance as shown in figure below due to different resolutions, simplification of physicals etc. Ensemble approach from many model forecasts is used in current NHC operation to guidance in the preparation of official track and intensity forecasts. 

<img src="http://icons.wxug.com/hurricane/2011/2010_skill.png" width="400"/>*Image credit: National Hurricane Center*

The objective here is to explore and develop deep neutral network to accurately:

- estimate the intensity of the TCs based on the satellite images;

- forecast the track of the TCs from the advisory information (location, maximum speed, radius etc.);

- and ultimately, forecast the track and characteristics of the TCs based on the satellite images

which is referred as deepTC. The development of deepTC is primary carried out on Google Colab and organized into following notebooks,

1. Data Preprocess
   - 1.1 [Satellite images and tracks of TCs](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_images_tracks_sync.ipynb/)

   - 1.2 [Statistics of satellite images and tracks](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_images_tracks_stats.ipynb)

2. Model for TC Intensity
   - 2.1 [Post-binding architecture of TC Intensity](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_net_intensity.ipynb)

   - 2.2 [CNN model for intensity classification](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_cnn5_classification.ipynb)

   - 2.3 [Resnet model for intensity classification](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_resnet_classification.ipynb)

   - 2.4. [Resnet model for TC intensity estimation](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_resnet_intensity.ipynb)

3. [DCGAN model for deepTC](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_dcgan.ipynb)

4. Model for TC Track
    - 4.1 [Post-binding architecture of TC Track](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_net_track.ipynb)
    
    - 4.2 [LSTM model for TC track prediction](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_lstm_track.ipynb)
 
    - 4.3 [LSTM-CNN model for TC track prediction](https://github.com/aachen6/deepTC/blob/master/colab/deepTC_lstmcnn_track.ipynb)
