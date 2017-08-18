![DBG](images/dbg-horizontal.png)

# Change Point Detection in Time Series Sensor data

Offering Managers: Manjula Hosurmath (Business Unit)

Development: Vishal Chahal, Krishna Prabu, Shikha Maheshwari

August 17, 2017

![DBG](images/dbg-vertical.png)

&nbsp;
&nbsp;
&nbsp;
&nbsp;

## Overview

This journey takes you through end to end flow of steps in collating statistics on Time series data and identify if a Change point has occurred. Core building blocks include computing Statistical parameters from the Time series data, which compares a Previous dataset of a certain Time range in the past with the Current Series in a recent Time range, and statistical comparison between these two results in detection of any change points. R statistical software is used in this Journey with sample sensor data loaded into the Data Science Experience cloud. 

In this journey we will demonstrate:
*	Data acquisition and storage of IoT Sensor data using Node Red flows and DB2 Warehouse on Cloud
*	Data retrieval and statistical Change point detection using R - Jupyter notebooks	
	-	Create and Run a Jupyter Notebook in DSX
	-	Run R statistical software code in Jupyter Notebook
	-	Read data from database in R notebook and statistically analyze the data
	-	Execute R statistical functions to detect Change point in data
*	Generate results in the form of visualisation plots and save results in DSX Jupyter Notebook

## Architecture Diagram

![Architecture](images/architecture.png)

## IBM Products
* [IBM Node-RED Cloud Foundry App](https://console.bluemix.net/catalog/starters/node-red-starter): Develop, deploy, and scale server-side JavaScript® apps with ease. The IBM SDK for Node.js™ provides enhanced performance, security, and serviceability.
* [IBM Data Science Experience](https://www.ibm.com/bs-en/marketplace/data-science-experience): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.
* [DB2 Warehouse on cloud](https://console.bluemix.net/catalog/services/db2-warehouse-on-cloud): IBM Db2 Warehouse on Cloud is a fully-managed, enterprise-class, cloud data warehouse service. Powered by IBM BLU Acceleration.
* [Bluemix Object Storage](https://console.ng.bluemix.net/catalog/services/object-storage/?cm_sp=dw-bluemix-_-code-_-devcenter): A Bluemix service that provides an unstructured cloud data store to build and deliver cost effective apps and services with high reliability and fast speed to market.
* [Internet of Things Platform](https://console.bluemix.net/catalog/services/internet-of-things-platform): This service is the hub for IBM Watson IoT and lets you communicate with and consume data from connected devices and gateways. Use the built-in web console dashboards to monitor your IoT data and analyze it in real time.

## Related Technologies

* [Jupyter Notebooks](http://jupyter.org/): An open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.
* [R](https://www.r-project.org/): R is an open source programming language and software environment for statistical computing and graphics that is supported by the R Foundation for Statistical Computing.
* [Data Science](https://developer.ibm.com/code/technologies/data-science/): Systems and scientific methods to analyze structured and unstructured data in order to extract knowledge and insights.


## Key Features

* Statistical method for detecting Change point in Time stamped Sensor data.
* Execute R statistical functions in Jupyter Notebook to detect Change point in data.
* Works as-is for any type of sensor.
* All components are made completely configurable so that multiple experiments can be repeated by tweaking the parameters.

## Rationale

As IoT solutions emerge, the amount of available sensor data is growing. Sensors collect and transmit data on a continuous basis which is Time stamped. It usually requires real-time analysis and decision making. The traditional approach is to use a rules-based engine, which triggers alerts according to some manually configured thresholds. The statistical method for detecting Change point in Sensor data will be beneficial to get more accurate results for time series data.

This journey helps in collating statistics on the Time series data and identify if a Change point has occurred.

## Journey Hypothesis

### Opportunity

* Data scientist and IoT solution developers who wants to experiment, learn, enhance and implement a new method for Statistically detecting Change point in Sensor data.

### Operational Efficiency

* Data retrieval and statistical analysis using R - Jupyter notebooks to analyze data.
* Highlights developer productivity – minimal programming effort and reduced development time.

### Community and Advocacy

* Customers interested in doing statistical analysis of time stamped sensor data.
* All components are made completely configurable so that the developers can do multiple experiments by tweaking the parameters. It opens a world of possibilities for developers.
* IBM Data Science Experience provides an environment where the developers can collaborate to analyze and visualize their data with Jupyter notebooks that run on Spark. RStudio, included in IBM Data Science Experience, provides an IDE for working with R. It reduces a lot of configuration and development effort and increases productivity.

### Amplification

* Opens up the channel to do more statisitical analysis using Data Science Experience to analyze IoT sensor data.
* Demos at target conferences and meetups to find partners.
* Integrate with other Bluemix services to add more insights and deliver the solution.

### Competition

***** The other solutions to integrate IBM Data Science experience with a custom UI is time consuming to build but can offer more flexibility

## Concept

### What is the Journey?

Change point detection is used to detect any abrupt changes in Time Series data. Specifically, in IoT Sensor data the applications are very wide. This journey takes you through end to end flow of steps in collating statistics on such Time series data and identify if a Change point has occurred. R statistical software is used in this Journey with sample Sensor data loaded into the Data Science experience cloud. 

This journey leverages Node-RED in IBM Bluemix and R Spark services in IBM Data science experience at its core to implement.

The steps are detailed below:
	
1. Collects data from a IoT Sensor source (IoT sensor data acquisition is simulated in this journey through Node-RED) and injects into a DB2 database in cloud.
2. Extract 2 Time series datasets one in the past and another in the present.
3. Compress these datasets by translating them into a bunch of statistics that accurately describe the characteristics of these datasets.
4. Compare these statistics and quantify them Analyze these comparisons to detect any occurrence of Change points in the data between Previous data set and Current data set.

### Who is it for?

IoT Solution Developers and Data scientist who who wants to learn, enhance and implement a new method for Statistically detecting Change point in Sensor data.

### What will they learn?
* Development using R statistical functions written in R Spark – Jupyter Notebook in IBM Data Science Experience.
* Write data from a IoT source to a database using Node-RED.
* Execution of R statistical functions to detect Change point in data.
* ****Visualization of the results from DSX.

## What does it look like?

1. Provision Node-RED starter, Object Storage, DB2 Warehouse on Cloud, Internet of Things Platform, Apache Spark Service.
2. Store sensor data documents in Object storage.
3. Add object storage and watson IoT nodes in Node-RED editor.
4. Import the Node-RED flow json into the Node-RED editor. Configure (set credentials) for object storage, Watson IoT, IBM IoT, and dashDB node. Deploy the Node-RED flow.
5. Import the Jupyter notebook into Data Science Experience. Change DB2 Warehouse on Cloud credentials.****
6. Upload the sample .json DSX configuration file to Object storage.
7. Execute the notebook.
8. Outputs the results in the Notebook which can be copied to clipboard and visualize.

# Strategy

## What is the strategy?

Sensors mounted on devices like IoT devices, Automated manufacturing like Robot arms, Process monitoring and Control equipment etc., collect and transmit data on a continuous basis which is Time stamped. The amount of available sensor data is continuously growing and it requires real-time analysis. Change point detection is used to detect any abrupt changes in Time Series data. Traiditional Change point detection that are implemented use Rule based methods that compare 2 data points or sets of 2 time series to compare and detect if there is a significant change that had taken place. This Journey uses Statistical approach to detect such change points.

This journey helps in collating statistics on the Time series data and identify if a Change point has occurred. The feedback has been positive with SI partners - Cap Gemini, Infosys, Tech Mahindra, Wipro.

## What is the advocacy potential?

The potential is high. It demonstrates the ability to do statistical analysis using IBM Data Science Experience. 

## What are some target events or meetups?

DevOps, Serverless, and Open Source meetups and conferences with rapid app development focus:

* DevOps Days (many worldwide)
* Container Camp AU (5/22-24)
* Cloud Expo NYC (6/6)
* OSCON (5/10)
* OSCON EU (11/6)
* Open Source Summit LA (9/11-13)
* Open Source Summit Tokyo (5/31)
* Open Source Summit Europe (10/23)
* CloudNativeCon / KubeCon Austin (12/6)
* ApacheCon North America (5/16)
* Serverless Conf (4/26)
* Serverless Conf Europe (10/24)
* Kafka Summit SF (8/28)

## How does this impact the city and community Heat Maps?



## What are the key metrics for this Journey?

1. \# Github repo forks
2. \# Readme page views
3. % reduction in churn from monthly active users (MAU) versus non-Journey MAU

