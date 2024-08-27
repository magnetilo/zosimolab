# ZosimoLabs

ZosimoLabs is a single headed company by Thilo Weber.
````
Data is the new gold! 
You just need an alchemist. 
It’s possible. Ask Zosimo the alchemist.
````

-----

# Offerings

## Machine Learning and Data Science Consulting
- **Data Analysis and Visualization:** Create and enhance understanding of complex processes and problems through analyzing monitoring datasets.  Example projects: [Energy efficiency monitoring and root cause analysis](#energy-efficiency-monitoring-and-root-cause-analysis), “Time-to-event prediction & survival analysis”, “Model-based signal processing & sparse priors”
- **Monitoring and Predictive Modeling:** Build up monitoring for indicators of interest and develop predictive models to forecast demands, trends, customer behaviors, and more. Example projects: “Energy and CO2 monitoring for municipalities”, “Energy efficiency monitoring & root cause analysis”
- **Natural Language Processing (NLP):** Implement NLP solutions for analyzing and structuring unstructured data and developing chatbots.  Example projects: “Address matching service”, ... currently working on a RAG-chatbot  project
- **Computer Vision:** Create image and video analysis models for applications in security, healthcare, retail, etc.  Example projects: “Image segmentation from classification labels only”
- **Recommendation Systems:** Build personalized recommendation engines to support workflow of sales and operations employees, or enhance user experiences in e-commerce and content platforms.  Example projects: “Machine learning-based lead generator (or recommender system)”, “Time-to-event prediction & survival analysis”

## Innovative Prototype Development
- **Prototype Ideation:** Generate creative, data-driven ideas that can be transformed into innovative prototypes.
- **Rapid Prototyping:** Develop quick prototypes using machine learning and data science techniques to validate concepts.
- **Proof of Concept (PoC) Development:** Create PoCs to demonstrate the feasibility and value of innovative ideas.

## Custom AI Solutions
- **Automation of Business Processes:** Develop AI-driven automation tools that streamline workflows and reduce operational costs.
- **Custom Machine Learning Algorithms:** Design and implement bespoke machine learning algorithms tailored to specific business needs.
- **AI-Driven Product Development:** Assist in the creation of AI-infused products that leverage data for enhanced functionality.

## Creative Consulting
- **Innovation Workshops:** Conduct workshops to help teams to generate creative data use cases and to integrate machine learning into their workflows / solutions. 
- **Strategic Advisory:** Provide strategic advice on how businesses can leverage data science and AI for innovation.

-----

# Example Projects

* [Energy efficiency monitoring and root cause analysis](#energy-efficiency-monitoring-and-root-cause-analysis)
* [Energy and CO2 monitoring for municipalities](#energy-and-CO2-monitoring-for-municipalities)
* [Model-based signal processing and sparse priors](#model-based-signal-processing-and-sparse-priors)

## Energy efficiency monitoring and root cause analysis

### Description:
At geoimpact, I developed machine learning models for predicting the yearly heat and electricity demands of buildings. In the context of a Master’s thesis, we used these models to estimate the actual reduction in yearly heat consumption effected by different renovation measures (roof/facade insulation, window replacement, ...). This framework can be used to build a monitoring of the effects of different measures applied to buildings in a portfolio or a region.

### Methods:
* **Partial dependence:** The plots below show the partial dependence of the heat consumption indicator (HCI) on construction year and heating degree days.
* **Combining domain knowledge & ML:**  In the plots below, the lines of the linear model and the neural network, which both integrate domain knowledge in the model architecture, show more realistic dependencies than the gradient boosting (without domain knowledge).

### Specials:
Apart from efficiency monitoring, such a framework can be used for a general root cause analysis of physical processes. For example, I introduced the framework to a friend who is working for a big chemical industry company. He quickly gained a lot of valuable insights into their production processes from it. He is since known as “the data leech” at his company.

### Technology:
Python, Scikit-Learn, Tensorflow, MLflow, PostgreSQL, Kubernetes

### Links:
* [Blog heat demand model](https://www.swissenergyplanning.ch/post/machine-learning-based-heat-demand-model)
* ... a paper presenting the framework is in progress in collaboration with Hochschule Luzern.

![Framework diagram](/img/framwork_schema.png)

![Partial dependences for different input features](/img/pdp_heat_demand_indicator.png)

-----

## Energy and CO2 monitoring for municipalities

### Description:
At geoimpact, in collaboration with the Federal Office of Energy, we developed the public web application Energy Reporter, which monitors the progress of all Swiss municipalities in the energy transition. I was responsible for the design and deployment of the methodology and data pipeline that imports public datasets and updates the six indicators every week. The indicators of Energy Reporter are published as open data. Building on the Energy Reporter, I further developed a comprehensive energy and CO2 monitoring containing over fifty fine granulated indicators, among which also the scope 1 and 2 CO2 emissions per municipality and year.

### Methods:
This project involved reasearching and processing of many different public data sources. Especially the two indicators for electricity consumption and renewable electricity production rely on statistical models that build on more than ten different data sources each.

### Specials:
The Energy Reporter is widely used by the public, especially by municipal officers and the media. It’s open data is used by many Swiss medias such as SRF, 20 min, Watson, and many local news papers. It uses an unconventional data visualization method encouraging users to interactively compare different municipalities, inspired by the Quartett card game.

### Technology:
Python, Pandas, Scikit-Learn, PostgreSQL, Kubernetes, Hangfire

### Links:
• [Energie Reporter Web-app](https://www.energiereporter.ch)
• [Energie Reporter Methodology](https://energiereporter.energyapps.ch/methodology)
• [Energie Reporter open data](https://opendata.swiss/en/dataset/energie-reporter)

![Energie Reporter](/img/energiereporter.png)

-----

## Model-based signal processing and sparse priors

### Description:
In my Master’s thesis at ETH Zurich, I used statistical signal processing methods for separating positional eye movement measurements into different types (saccades, smooth pursuit, and fixation eye movements). I developed a novel approach to precessing eye movement signals based on estimating signals in a mechanistic physiological model of the eye muscles. Apart from signal separation, the framework is also able to estimate the neural inputs into the eye muscles from the positional measurements.

### Methods:
• **Factor graphs:** They are a powerful probabilistic framework for working with structured models and has many applications, e.g., state space models, image models, error correcting codes, optimal control.
• **Sparse Bayesian learning:** This is a widely applicable and efficient method for modeling and estimating sparse (non-gaussian) priors in a probabilistic framework, which we applied to factor graphs.

### Specials:
I made especially two contributions in my thesis: Firstly, the usage of a new sparsity prior within the factor graph framework, which allowed to appropriately set the sparsity level. Secondly, the usage of existing mechanistic eye movement models, which have been developed since the 1980s, for solving this problem.

### Technology:
Matlab

### Links:
• [Journal paper: Model-based separation, detection and classification of eye movements](https://doi.org/10.1109/TBME.2019.2918986)
• [Code github](https://github.com/magnetilo/mbsdc_code)

![mbsd_framework](/img/mbsd_framework.png)

![eye_movement_separation](/img/eye_movement_separation.png)

-----

## Machine learning-based lead generator (or recommender system)

### Description:
At geoimpact, I developed a lead generator that suggests promising buildings for the sale of a renewable energy product based on a list of past sales of the product.

### Methods:
• **Thompson sampling:** This is a method for addressing the exploration- exploitation tradeoff in contextual bandit problems, where we want to maximise a certain reward (i.e., contacting the most promising building owners) and at the same time to continuously improve our model predicting the reward.
• **Extra trees classifier:** I used a simple implementation of Thompson sampling by sampling different trees of an extra tree classifier.
• **Supervised clustering:** The extra tree classifier can also be used to create cluster of buildings that behave “similar” with respect to this sales-problem. These cluster were used for a stratified sampling approach that helps to enhance the diversity in the potential customer exploration. The plot below shows a similarity matrix clustered into ten clusters of “similar” buildings.

### Specials:
We tested this method with a company selling photovoltaic systems. The project was stopped after the testing phase, as the cold acquisition process was too tedious. Here, I learned that a method can be theoretically very elaborated, but in the end it still needs to fit well into an end-to-end business workflow in order to be practical.

### Technology:
Python, Scikit-Learn

### Links:
• [Blog: Machine learning for MarketSense](https://www.swissenergyplanning.ch/post/machine-learning-for-marketsense-1)

![similarity_clustering](/img/similarity_clustering.png)

-----

## Time-to-event prediction & survival analysis

### Description:
At geoimpact, I developed multiple models for estimating the renovation pressure of a building. The underlying problem structure of calculating the time until a certain event happens has a variaty of applications apart from renovation rates in industry, medicine, churn rate (in e-commerce and human resources), and more.

### Methods:
There are different ways to mathematically express such a pressure. We explored two approaches:
• **Cox hazard model**
• **Conditional density estimation** using neural networkds for calculating context- dependent survival functions

### Specials:
The developed renovation pressure model has been integrated by different real- estate companies into their workflows and services.

### Technology:
Python, lifelines, TensorFlow Probability

### Links:
• [Blog: Sanierungsdruck auf Gebäudeebene](https://www.swissenergyplanning.ch/post/sanierungsdruck-auf-gebäudeebene-1)
• [Master Thesis Sarah Schneeberger: Energetic Restoration Pressure](https://github.com/Pflotsch/Energetic-Restoration-Pressure-Thesis/blob/master/Energetic_Restoration_Pressure.pdf)
