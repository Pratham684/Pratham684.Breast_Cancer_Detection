# Detecting Breast Cancer using Neural Nets

## What is the Project all about?
In India and over the world, Cancer has become a deadly disease and more and more people are suffering from Cancer and a survey says one in every 30 women suffer from this disease in their lifetime and so basically the project was first thought of because of the increase in cases of breast cancer and one thing which is very important that if we can detect the Cancer at an early stage then there is an increased chances of it getting cured.So this project lays a foundation in making the detection of the cancer automated so that more and more people can get it diagonised early so as get cured.

## How it is implemented?

The signs of detection are Masses and micro calcification clusters which are important in early detection of breast cancer.

Micro calcification are nothing but tiny mineral deposits within the breast tissue. They look similar to small white colored spots. They may or may not be caused by cancer.

Masses can be many things, including cysts (fluid-filled sacs) and non-cancerous solid tumors, but they could also be cancerous.

The difficulty in cancer detection is that the abnormalities from normal breast tissues are hard to read because of their subtle appearance and ambiguous margins.Automated tools which can help radiologist in early detection of breast cancer.

Further we have classified the cancer into three categories after its detection- Normal,Malignant,Benign.

## Methodology
We have used adaptive mean filter to remove noise from image. Since it​ ​is​ ​better among​ ​all​ ​the​ ​spatial​ ​filters​ ​and​ ​distinguish​ ​fine​ ​details from noise.
The Adaptive Median Filter performs spatial processing​ ​to​ ​determine​ ​which​ ​pixels​ ​in​ ​an​ ​image have​ ​been​ ​affected​ ​by​ ​impulse​ ​noise.​ ​The​ ​Adaptive​ ​Median​ ​Filter​ ​classifies​ ​pixels as​ ​noise​ ​by​ ​comparing​ ​each​ ​pixel​ ​in​ ​the​ ​image​ ​to​ ​its​ ​surrounding​ ​neighbor​ ​pixels. 

The​ ​size​ ​of​ ​the​ ​neighborhood​ ​is​ ​adjustable,​ ​as​ ​well​ ​as​ ​the​ ​threshold​ ​for​ ​the comparison.​ ​A​ ​pixel​ ​that​ ​is​ ​different​ ​from​ ​a​ ​majority​ ​of​ ​its​ ​neighbors,​ ​as​ ​well​ ​as being​ ​not​ ​structurally​ ​aligned​ ​with​ ​those​ ​pixels​ ​to​ ​which​ ​it​ ​is​ ​similar,​ ​is​ ​labeled​ ​as impulse​ ​noise.

​These​ ​noise​ ​pixels​ ​are​ ​then​ ​replaced​ ​by​ ​the​ ​median​ ​pixel​ ​value​ ​of the​ ​pixels​ ​in​ ​the​ ​neighborhood​ ​that​ ​have​ ​passed​ ​the​ ​noise​ ​labeling​ ​test.we​ ​are initially​ ​converting​ ​the​ ​image​ ​into​ ​grayscale​ ​image​ ​using​ ​rgb2gray()​ ​function​ ​then ​​applying​ ​adaptive​ ​mean​ ​filtering​ ​to​ ​the​ ​resulting​ ​image​ ​and​ ​then​ ​converted​ ​the image​ ​into​ ​unsigned​ ​integer​ ​8​ ​using​ ​unit8()​ ​function.

​In​ ​this​ ​way​ ​we​ ​preprocessed image.then​ ​we​ ​performed​ ​GMM​ ​segmentation(Gaussian​ ​Mixture​ ​Model)​ ​on​ ​the preprocessed​ ​image​ ​with​ ​number​ ​of​ ​regions​ ​2​ ​and​ ​number​ ​of​ ​GMM​ ​components 2​ ​and​ ​maximum​ ​number​ ​iterations​ ​10.​ ​we​ ​performed​ ​k-means​ ​segmentation​ ​with k=2.​ ​then​ ​we​ ​Implemented​ ​HMRF-EM​ ​(Hidden Markov Random Field Model) and its Expectation-Maximization Algorithm. 

 

## How to make the project work?

Open the project in matlab and then run **`guidemo.m`** and then a gui mode window will open and then just follow the steps there.For further information check the screenshots.

## NOTE: [](url)Kindly install MATLAB's [Wavelet Toolbox](https://in.mathworks.com/products/wavelet.html)
