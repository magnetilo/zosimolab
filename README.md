# ZosimoLab

ZosimoLab is a data and knowledge company by Thilo Weber.
````
Data is the new gold! 
You just need an alchemist. 
It’s possible. Ask Zosimo the Alchemist.
````

- [Services](#services)
- [Example Projects](#example-projects)
- [About](#about)
- [Partners](#partners)
- [Blog](#blog)
- [Contact](#contact)

-----

# Services

- **Implementing custom AI & ML solutions**:
  - **Real estate and energy data**: Profound knowledge of available data sources (especially in Switzerland), and how to extract value from them.
  - **Geo-spatial data**: Answering questions with geo-spatial datasets.
  - **Time-series data**: Data modelling and analysis of temporal signals.
  - **Unstructured data**: Extracting structured information and thereby value from unstructured documents, such as PDFs, images, Word-documents, ...
  - **Predictive modeling**: Probabilistic modelling of real world processes (mechanistic, biological, statistical, chemical, physical, ...).
  - **Computer vision**: Extracting information from images and raster data.
  - **Natural language processing and chatbots**: Text classification, RAG and AI-assinstant prototypes for answering questions from documents or webpages, ...
- **Strategic advisory and creative workshops**:
  - **Converting data to gold**: How to unlock the value hidden in your data with ML & AI & data analytics?
  - **Evaluation-driven development**: How to sustainably develop AI & ML solutions in presence of uncertainty in model results?
  - **Productionize**: How to bring AI & ML solutions into products and workflows?

[Jump to top](#zosimolab)

-----

# Example Projects

* [Parsing Ustructured PDFs & Information Extraction from Documents](#parsing-ustructured-pdfs-information-extraction-from-documents)
* [Energy Efficiency Monitoring and Root Cause Analysis](#energy-efficiency-monitoring-and-root-cause-analysis)
* [Energy and CO2 Monitoring for Municipalities](#energy-and-CO2-monitoring-for-municipalities)
* [Model-based Signal Processing and Sparse Priors](#model-based-signal-processing-and-sparse-priors)
* [Machine Learning-based Lead Generator (or Recommender System)](#machine-learning-based-lead-generator-(or–recommender-system))
* [Time-to-Event Prediction and Survival Analysis](#time-to-event-prediction-and-survival-analysis)
* [Image Segmentation from Classification Labels only](#image-segmentation-from-classification-labels-only)

-----

## Parsing Ustructured PDFs & Information Extraction from Documents

### Description:
For [Demokratis](https://www.demokratis.ch/), I helped to make Legislative Consultation PDFs more accessible and interactive by parsing them into a structured data form using AI. I employed an evaluation driven development approach, that helps to navigate tha landscape of innumerable possible parsing solutions.

### Methods:
* **Evaluation driven Generative AI**: Constructing numeric and visual evaluation metrics using Python's difflib and tracking experiment code and results in MLflow.
* **LlamaParse**: Powerful AI tool for extracting data from documents, such as PDFs.
* **ChatGPT API with file upload**: Another approach evaluated, but less suited for this particular problem.

### Specials:
Similar approaches can used to bring a wide range of real world data and documents into a structured form, building the basis for a variety of data analysis and processing use cases.

### Technology:
Python, LlamaParse, openai APIs, MLflow, difflib

### Links:
* [Blog: Parsing Legislative Consultation PDFs Using LlamaParse](https://medium.com/@thiloweber/parsing-legislative-consultation-pdfs-using-llamaparse-fdd4627b9094)

![Difflib HTML comparison](/img/output-difflib-html.png)

[Jump to top](#zosimolab)

-----

## Energy Efficiency Monitoring and Root Cause Analysis

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

[Jump to top](#zosimolab)

-----

## Energy and CO2 Monitoring for Municipalities

### Description:
At geoimpact, in collaboration with the Federal Office of Energy, we developed the public web application Energy Reporter, which monitors the progress of all Swiss municipalities in the energy transition. I was responsible for the design and deployment of the methodology and data pipeline that imports public datasets and updates the six indicators every week. The indicators of Energy Reporter are published as open data. Building on the Energy Reporter, I further developed a comprehensive energy and CO2 monitoring containing over fifty fine granulated indicators, among which also the scope 1 and 2 CO2 emissions per municipality and year.

### Methods:
This project involved reasearching and processing of many different public data sources. Especially the two indicators for electricity consumption and renewable electricity production rely on statistical models that build on more than ten different data sources each.

### Specials:
The Energy Reporter is widely used by the public, especially by municipal officers and the media. It’s open data is used by many Swiss medias such as SRF, 20 min, Watson, and many local news papers. It uses an unconventional data visualization method encouraging users to interactively compare different municipalities, inspired by the Quartett card game.

### Technology:
Python, Pandas, Scikit-Learn, PostgreSQL, Kubernetes, Hangfire

### Links:
- [Energie Reporter Web-app](https://www.energiereporter.ch)
- [Energie Reporter Methodology](https://energiereporter.energyapps.ch/methodology)
- [Energie Reporter open data](https://opendata.swiss/en/dataset/energie-reporter)

![Energie Reporter](/img/energiereporter.png)

[Jump to top](#zosimolab)

-----

## Model-based Signal Processing and Sparse Priors

### Description:
In my Master’s thesis at ETH Zurich, I used statistical signal processing methods for separating positional eye movement measurements into different types (saccades, smooth pursuit, and fixation eye movements). I developed a novel approach to precessing eye movement signals based on estimating signals in a mechanistic physiological model of the eye muscles. Apart from signal separation, the framework is also able to estimate the neural inputs into the eye muscles from the positional measurements.

### Methods:
- **Factor graphs:** They are a powerful probabilistic framework for working with structured models and has many applications, e.g., state space models, image models, error correcting codes, optimal control.
- **Sparse Bayesian learning:** This is a widely applicable and efficient method for modeling and estimating sparse (non-gaussian) priors in a probabilistic framework, which we applied to factor graphs.

### Specials:
I made especially two contributions in my thesis: Firstly, the usage of a new sparsity prior within the factor graph framework, which allowed to appropriately set the sparsity level. Secondly, the usage of existing mechanistic eye movement models, which have been developed since the 1980s, for solving this problem.

### Technology:
Matlab

### Links:
- [Journal paper: Model-based separation, detection and classification of eye movements](https://doi.org/10.1109/TBME.2019.2918986)
- [Code github](https://github.com/magnetilo/mbsdc_code)

![mbsd_framework](/img/mbsd_framework.png)

![eye_movement_separation](/img/eye_movement_separation.png)

[Jump to top](#zosimolab)

-----

## Machine Learning-based Lead Generator (or Recommender System)

### Description:
At geoimpact, I developed a lead generator that suggests promising buildings for the sale of a renewable energy product based on a list of past sales of the product.

### Methods:
- **Thompson sampling:** This is a method for addressing the exploration- exploitation tradeoff in contextual bandit problems, where we want to maximise a certain reward (i.e., contacting the most promising building owners) and at the same time to continuously improve our model predicting the reward.
- **Extra trees classifier:** I used a simple implementation of Thompson sampling by sampling different trees of an extra tree classifier.
- **Supervised clustering:** The extra tree classifier can also be used to create cluster of buildings that behave “similar” with respect to this sales-problem. These cluster were used for a stratified sampling approach that helps to enhance the diversity in the potential customer exploration. The plot below shows a similarity matrix clustered into ten clusters of “similar” buildings.

### Specials:
We tested this method with a company selling photovoltaic systems. The project was stopped after the testing phase, as the cold acquisition process was too tedious. Here, I learned that a method can be theoretically very elaborated, but in the end it still needs to fit well into an end-to-end business workflow in order to be practical.

### Technology:
Python, Scikit-Learn

### Links:
- [Blog: Machine learning for MarketSense](https://www.swissenergyplanning.ch/post/machine-learning-for-marketsense-1)

![similarity_clustering](/img/similarity_clustering.png)

[Jump to top](#zosimolab)

-----

## Time-to-Event Prediction and Survival Analysis

### Description:
At geoimpact, I developed multiple models for estimating the renovation pressure of a building. The underlying problem structure of calculating the time until a certain event happens has a variaty of applications apart from renovation rates in industry, medicine, churn rate (in e-commerce and human resources), and more.

### Methods:
There are different ways to mathematically express such a pressure. We explored two approaches:
- **Cox hazard model**
- **Conditional density estimation** using neural networkds for calculating context- dependent survival functions

### Specials:
The developed renovation pressure model has been integrated by different real- estate companies into their workflows and services.

### Technology:
Python, lifelines, TensorFlow Probability

### Links:
- [Blog: Sanierungsdruck auf Gebäudeebene](https://www.swissenergyplanning.ch/post/sanierungsdruck-auf-gebäudeebene-1)
- [Master Thesis Sarah Schneeberger: Energetic Restoration Pressure](https://github.com/Pflotsch/Energetic-Restoration-Pressure-Thesis/blob/master/Energetic_Restoration_Pressure.pdf)

![renovpress](/img/renovpress.png)

[Jump to top](#zosimolab)

-----

## Image Segmentation from Classification Labels only

### Description:
At geoimpact, I developed a model for detecting photovoltaic (PV) systems in satellite images and estimating their area. The plan was to extract a Swiss-wide data base with all installed PV-systems and their installed capacity from arerial and satellite images.

### Methods:
- **Convolutional neural networks (ConvNet):** They are a special sort of neural networks that are especially useful for different image and video tasks, such as, object detection, segmentation, image descriptions, and more.
- **Class activation mappings (CAM):** While the most common approach of semantic segmantation would require to manually mark a lot of PV systems with polygons in target images, I used a special approach based on class activation mappings (CAM) that required only classification labels if an image contains a PV system or not.

### Specials:
Soon after we started the project, the Swiss Federal Office of Energy published an open data set containing all registered PV systems registered, which made our project basically obsolete. Here I learned, that there are often different ways to acquire a specific dataset. Sometimes, there are probably simpler and more accurate acquisition methods than rather complex image detection approaches.

### Technology:
Python, PyTorch, OpenCV

![test_CAM](/img/test_CAM.jpg)

[Jump to top](#zosimolab)

-----

# About

![outer-inner-knowledge](/img/ZosimoLab-outer-inner-knowledge.png)

> ca. 300: Zosimos of Panopolis (also known by the Latin name Zosimus Alchemista) was an alchemist living in the south of then Roman Egypt who wrote the oldest known books on alchemy. Alchemists were striving for understanding external and internal nature. In particular, one quest was the transformation of cupper into gold through a process of purification. This process of purifying external nature was thought to be mirrored by a process of purifying internal nature, where the quest was to draw the spirit from its bondage with bodies.
> 
> 1718: Zosimo was a farmer living in Sicily who was elected king by the people. The people of Sicily were at the time controlled by Spanish oppressors. Zosimo started a revolution that brought the power back to the people, at least for a short period of time. I like to think of him as a social transformer or alchemist. There is a book written about his story by Andrea Camilleri as well as a song by the band Il Coccodrillo.
> 
> 2024: The first alchemists' strive for understanding and purifying external nature evolved into a deep understanding of and ability to control physical nature, resulting in trains, cars, electrical devices and many useful things. In a new age of data and artificial intelligence, we arrive at understanding and controlling another level of nature: the level of thoughts and information. ZosimoLab is founded to assist you in realizing the vast possibilities hidden on this level of thoughts and information - and thereby transforming your data into gold.

About me:
My name is Thilo Weber, I have a Msc. in electrical engineering and information processing from ETH Zurich, and several years of experience in realizing data science and machine learning projects in the industry. Trough ZosimoLab, I want to share my passion for understanding the world through data with you, and help you to create great machine learning solutions. Further, I would also like to share my process of inner alchemy by embedding the current progress in data science and artificial intelligence in a phsychological and philosophical understanding.

![kl_portrait](/img/portrait-tarasp.png)

[Jump to top](#zosimolab)

-----

# Partners

To create optimal solutions on larger data projects, I work with dedicated implementation partners:
- Joris Noordermeer, Web Development, [https://noordermeer.ch/](https://noordermeer.ch/)
- Aarefabrik, Mobile Apps & Web Development, [https://aarefabrik.ch/](https://aarefabrik.ch/)
- Datali, Data Solutions, [https://datali.ch/](https://datali.ch/)

[Jump to top](#zosimolab)

-----

# Blog

I am writing about my projects, knowledge of the world, and self-knowledge on [Medium](https://medium.com/@thiloweber).

- [Parsing Legislative Consultation PDFs Using LlamaParse](https://medium.com/@thiloweber/parsing-legislative-consultation-pdfs-using-llamaparse-fdd4627b9094)
- [A Yogic Perspective on Artificial Intelligence: Bridging Consciousness and Technology](https://medium.com/@thiloweber/a-yogic-perspective-on-artificial-intelligence-bridging-consciousness-and-technology-5ce1449544f1)
- [Why AI is Not Intelligent](https://medium.com/@thiloweber/why-ai-is-not-intelligent-2aa0427f47e9)
- [The Path of Relationship](https://medium.com/@thiloweber/the-path-of-relationship-b7d540173aac)
- [Towards Physics, Towards Data Science, and Beyond](Towards Physics, Towards Data Science, and Beyond)
- [Our Daily Cycles of Aversion From and Attachment To Work](https://medium.com/@thiloweber/our-daily-cycles-of-aversion-from-and-attachment-to-work-and-how-content-platforms-are-helping-bc89bad3614c)

[Jump to top](#zosimolab)

-----

# Contact

- contact@zosimolab.com
- [freelancermap profile](https://www.freelancermap.ch/profil/thilo-weber)

[Jump to top](#zosimolab)


