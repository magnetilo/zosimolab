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
- Data Analysis and Visualization: Create and enhance understanding of complex processes and problems through analyzing monitoring datasets.  Example projects: [Energy efficiency monitoring and root cause analysis](#energy-efficiency-monitoring-and-root-cause-analysis), “Time-to-event prediction & survival analysis”, “Model-based signal processing & sparse priors”
- Monitoring and Predictive Modeling: Build up monitoring for indicators of interest and develop predictive models to forecast demands, trends, customer behaviors, and more. Example projects: “Energy and CO2 monitoring for municipalities”, “Energy efficiency monitoring & root cause analysis”
- Natural Language Processing (NLP): Implement NLP solutions for analyzing and structuring unstructured data and developing chatbots.  Example projects: “Address matching service”, currently working on a RAG-chatbot (—> Learn more NLP processing.)
- Computer Vision: Create image and video analysis models for applications in security, healthcare, retail, etc.  Example projects: “Image segmentation from classification labels only”
- Recommendation Systems: Build personalized recommendation engines to support workflow of sales and operations employees, or enhance user experiences in e-commerce and content platforms.  Example projects: “Machine learning-based lead generator (or recommender system)”, “Time-to-event prediction & survival analysis”

## Innovative Prototype Development
- Prototype Ideation: Generate creative, data-driven ideas that can be transformed into innovative prototypes.
- Rapid Prototyping: Develop quick prototypes using machine learning and data science techniques to validate concepts.
- Proof of Concept (PoC) Development: Create PoCs to demonstrate the feasibility and value of innovative ideas.

## Custom AI Solutions
- Automation of Business Processes: Develop AI-driven automation tools that streamline workflows and reduce operational costs.
- Custom Machine Learning Algorithms: Design and implement bespoke machine learning algorithms tailored to specific business needs.
- AI-Driven Product Development: Assist in the creation of AI-infused products that leverage data for enhanced functionality.

## Creative Consulting
- Innovation Workshops: Conduct workshops to help teams to generate creative data use cases and to integrate machine learning into their workflows / solutions. (—> Ask Nora for tips / collaboration on creative workshops.)
- Strategic Advisory: Provide strategic advice on how businesses can leverage data science and AI for innovation.

-----

# Example Projects

## Energy efficiency monitoring and root cause analysis

### Description:
At geoimpact, I developed machine learning models for predicting the yearly heat and electricity demands of buildings. In the context of a Master’s thesis, we used these models to estimate the actual reduction in yearly heat consumption effected by different renovation measures (roof/facade insulation, window replacement, ...). This framework can be used to build a monitoring of the effects of different measures applied to buildings in a portfolio or a region.

### Methods:
* Partial dependence: The plots below show the partial dependence of the heat consumption indicator (HCI) on construction year and heating degree days.
* Combining domain knowledge & ML:  In the plots below, the lines of the linear model and the neural network, which both integrate domain knowledge in the model architecture, show more realistic dependencies than the gradient boosting (without domain knowledge).

### Specials:
Apart from efficiency monitoring, such a framework can be used for a general root cause analysis of physical processes. For example, I introduced the framework to a friend who is working for a big chemical industry company. He quickly gained a lot of valuable insights into their production processes from it. He is since known as “the data leech” at his company.

### Technology:
Python, Scikit-Learn, Tensorflow, MLflow, PostgreSQL, Kubernetes

### Links:
* Blog heat demand model: 
https://www.swissenergyplanning.ch/post/machine-learning-based-heat-demand-model
* ...a paper presenting the framework is in progress in collaboration with Hochschule Luzern.

![Framework diagram](/img/framwork_schema.png)

![Partial dependences for different input features](/img/pdp_heat_demand_indicator.png)

-----
