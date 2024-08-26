# projects

## Project: Energy efficiency monitoring & root cause analysis
### Description:
At geoimpact, I developed machine learning models for predicting the yearly heat and electricity demands of buildings. In the context of a Master’s thesis, we used these models to estimate the actual reduction in yearly heat consumption effected by different renovation measures (roof/facade insulation, window replacement, ...). This framework can be used to build a monitoring of the effects of different measures applied to buildings in a portfolio or a region.
### Methods:
* Partial dependence: The plots below show the partial dependence of the heat consumption indicator (HCI) on construction year and heating degree days.
* Combining domain knowledge & ML:  In the plots below, the lines of the linear model and the neural network, which both integrate domain knowledge in the model architecture, show more realistic dependencies than the gradient boosting (without domain knowledge).
### Specials:
Apart from efficiency monitoring, such a framework can be used for a general root cause analysis of physical processes. For example, I introduced the framework to a friend who is working for a big chemical industry company. He quickly gained a lot of valuable insights into their production processes from it. He is since known as “the data leech” at his company.
### Technology:
### Python, Scikit-Learn, Tensorflow, MLflow, PostgreSQL, Kubernetes
### Links:
* Blog heat demand model: 
https://www.swissenergyplanning.ch/post/machine-learning-based-heat-demand-model
* ...a paper presenting the framework is in progress in collaboration with Hochschule Luzern.

<img src="/img/framwork_schema.png" alt="Framework diagram" width="500"/>

![Partial dependences for different input features](/img/pdp_heat_demand_indicator.png)
