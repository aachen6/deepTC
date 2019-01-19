# DeepTC

Tropical Cyclones, hereafter referred to as TCs, are severe weather system originated over warm tropical ocean. They are known as hurricanes in the Atlantic and Northeast Pacific, cyclones in the South Pacific and Indian Ocean, and typhoons in the Northwest Pacific. TCs typically move from east to west due to the tropical trade winds near the equator where the TCs originate, and curve into higher latitude as a result of the Coriolis force and steering winds at higher elevation. Although the westerly winds prevail at higher altitude may steer the storm back to the east into the ocean and some of them may have weakened to a tropical storm or became extratropical, TCs may produce hurricane-force winds and storm surge along the coast even remained offshore or made direct landfall, which causes significant threat to life and property. For the TC warning and disaster management, the prediction of the intensity as well as the track of the TCs is very important for the local authorities in their decision making regarding the time and location of evacuation to reduce the potential damage due to the TCs.

The Dvorak technique is the most widely used methodology that estimates TC intensity, which correlates TC intensities to various cloud patterns of central and banding features in the infrared images from geostationary satellites. This technique suffers from subjectivity of the storm center selection and scene type determination procedures. Advanced Dvorak Technique for the estimation of TC intensity have been developed to reduce such subjectivity by using computer-based algorithms for recognizing cloud features, which is currently used in the NOAA operational model for estimation of storm intensity. However, such heuristic rule approach requires regional nuances and adjustment and always suffers from heuristic exception of rules that are not predefined. On the other hand, the prediction of TC track relies on numerical weather models such as the Weather Research and Forecasting (WRF) Model (WRF), Model for Prediction Across Scales (MPAS), and Community Atmosphere Model ver 5.0 (CAM5), which are expensive to run. Summary of Deep network for this task.

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/09/DvorakCDP1973.png/1280px-DvorakCDP1973.png" width="400"/>

The objective is to develop or explore deep neutral network to accurately:

- estimate the intensity of the TCs based on the satellite images;

- forecast the track of the TCs from the advisory information (location, maximum speed, radius etc.);

- and ultimately, forecast the track and characteristics of the TCs based on the satellite images

which is referred as deepTC. The development of deepTC is primary carried out on Google Colab and organized into following notebooks,

1. [Satellite images and tracks of TCs](https://)

2. [Statistics of satellite images and tracks](https://)

3. Architecture of deepTC
   * [Post-binding architecture for deepTC](https://)
   * [CNN/Resnet model for deepTC](https://)
   * [GAN model for deepTC](https://)
   * [LSTM model for deepTC](https://)
   * [LSTM-CNN model for deepTC](https://)

