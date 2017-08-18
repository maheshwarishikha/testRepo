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

* Method for detecting Change point in Time stamped Sensor data.
* Execute R statistical functions in Jupyter Notebook to detect Change point in data.
* Works as-is for any type of sensor.
* All components are made completely configurable so that multiple experiments can be repeated by tweaking the parameters.

## Rationale

As IoT solutions emerge, the amount of available sensor data is growing. Sensors collect and transmit data on a continuous basis which is Time stamped. It usually requires real-time analysis and decision making. The traditional approach is to use a rules-based engine, which triggers alerts according to some manually configured thresholds. The statistical method for detecting Change point in Sensor data will be beneficial to get more accurate results for time series data.

This journey helps in collating statistics on such Time series data and identify if a Change point has occurred.

## Journey Hypothesis

### Opportunity

* Data scientist and IoT solution developers who wants to experiment, learn, enhance and implement a new method for Statistically detecting Change point in Sensor data.

### Operational Efficiency

* Data retrieval and statistical analysis using R - Jupyter notebooks to analyze data.
* Highlights developer productivity – minimal programming effort and reduced development time.

### Community and Advocacy

* Customers interested in doing statistical analysis of time stamped sensor data.
* All components are made completely configurable so that the developers can do multiple experiments by tweaking the parameters. It opens a world of possibilities for developers.
* IBM Data Science Experience provides an environment where the developers can collaborate to analyze and visualize their data with Jupyter notebooks that run on Spark. RStudio, included in IBM Data Science Experience, provides an IDE for working with R. It reduces a lot of configuration and development effort and increses productivity.

### Amplification

* Opens up the channel to do more statisitical analysis using Data Science Experience to analyze IoT sensor data.
* Demos at target conferences and meetups to find partners.
* Integrate with other Bluemix services to add more insights and deliver the solution.

### Competition

***** The other solutions to integrate IBM Data Science experience with a custom UI is time consuming to build but can offer more flexibility

## Concept
As IoT solutions emerge, the amount of available sensor data is growing, but developing insight into that data can be difficult. Analyzing historical data is often the first step in understanding data you intend to use in real time. You may want to perform some basic statistics on your data to find 

Sensors collect and transmit data on a continuous basis which is Time stamped. Method for detecting Change point in Sensor data.

it usually requires real-time analysis and decision making. The traditional approach is to use a rules-based engine, which triggers alerts according to some manually configured thresholds. These systems lack data fusion and learning capabilities and therefore fail to cope with large amounts of complex high dimensional data.


This journey utilizes IoT sensor data and its primary goal is to statistically identify the change point in this sensor data rather than the acquisition and storage of the data itself. For sake of completeness of the flow, a simulation of the IoT data acquisition is included as a first step.

* Data acquisition and storage of IoT Sensor data using Node Red flows and DB2
* Data retrieval and statistical analysis using R - Jupyter notebooks to analyze and detect change points in the data

    Read Sensor data for a single sensor
    Extract 2 Time series datasets one in the past and another in the present
    Compress these datasets by translating them into a bunch of statistics that accurately describe the characteristics of these datasets
    Compare these statistics and quantify them Analyze these comparisons to detect any occurrence of Change points in the data between Previous data set and Current data set
### What is the Journey?

This project shows how Node-RED can be used to build a complete end to end analytics solution on IBM Data Science Experience(DSX) with a custom web user interface.

The steps are detailed below:
* The documents that require analysis are stored in Bluemix Object Storage.
* The python code retrieves the document content from Object storage.
* An event is triggered from the Web UI.
* The event is sent to the python code using web sockets.
* After the python code is executed on DSX, the response is sent to the websocket.
* The UI reads the response on the websocket and displays the results.

### Who is it for?

IoT Solution Developers and Data scientist who who wants to learn, enhance and implement a new method for Statistically detecting Change point in Sensor data.

### What will they learn?
From this journey, the developers will learn - 
*	Development on Data Science Experience using Python Pandas to derive insights on the data.
*	Development of a web user interface using Node-RED. 
* Triggering an analytics workflow on DSX from the UI and orchestration of the flow using Node-RED.
*	Visualization of the results from DSX on a custom web user interface

## What does it look like?

1. Provision Node-RED starter, Object Storage, Apache Spark Service
2. Store data documents in Object storage. 
3. Import the Jupyter notebook  into Data Science Experience. Enter credentials for Object storage and change web socket URL.
4. Import the Node-RED flow json into the Node-RED editor. Change the websocket URL and Deploy the Node-RED flow.
5. Execute all cells in the Jupyter notebook to start the web socket client.
6. The custom web user interface is rendered by Node-RED and is ready for use.

# Strategy

## What is the strategy?

The Data Science Experience (DSX) is designed to be used by Data Scientists.  It cannot be used to demonstrate the complete solution with a custom user interface.

This journey solves the need to develop a complete end to end analytics solution on IBM Data Science Experience that can be demonstrated. The feedback has been positive with SI partners - Cap Gemini, Infosys, Tech Mahindra, Wipro.



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

