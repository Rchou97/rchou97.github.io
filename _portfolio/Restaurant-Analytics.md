---
title: "Data Engineering within the hospitality industry"
excerpt: "A brief summary of the project that my brother and I am doing to perform analytics in the hospitality industry."
collection: portfolio
---
**July 2024**

Ever since I was young, I have always grown up within the restaurant industry. My parents always owned a restaurant or were working within the hospitality services. Since I have become older and gained theoretical and work experiences within the world of data, I became more aware of how much data can be extracted and used to increase decision-making of restaurant owners. My parents used their gut-feeling and/or a short horizon (approximately a week) to "forecast" how busy the restaurant may be. So it was not based on facts or figures. 

This leads to the personal project of my brother and me to initiate a platform for extracting and visualising data. He started the project by creating a front-end with Flask, JavaScript, Python and Google Sheets (not a massive fan of the last one, but he needed to start in some form or way). The first setup contained the turnover each day and some visualisations to present it: 

<img src='/images/example-dashboard.png' style="max-width: 100%; height: auto;">

After he managed to set up the first version, he was able to run the application locally in Flask. It was time for me to step in and create new data sources, create automated data pipelines and set up a platform for deployment. 

Design
------
The following tooling has been used for designing, managing and deploying the app and ETL services: 

* Google Cloud Platform
  * Platform
    * API & Services: for enabling the APIs needed to operate within the GCP platform.
    * App Engine: the service for publishing the app.
    * Billing: for monitoring the billing parts concerning the used cloud services.
    * Cloud Storage: storage for every used cloud service.
    * Cloud Run: service for operating the setup of Cloud Functions.
    * IAM & Admin: for providing and revoking access for different users and GCP services.
  * Data Engineering
    * BigQuery: used as data warehouse for analytics and powering the dashboard with data.
    * Cloud Functions: functions which are created in Python for the different ETL stages with all targeted to the BigQuery data warehouse.
    * Cloud Scheduler: the scheduled triggers for single Cloud Functions.
* Python
* SQL (BigQuery)

This can be translated in the following landscape architecture: 

<img src='/images/data-model-app-source-platform-landscape.png' style="max-width: 100%; height: auto;">

And for project management and documentation, the following tools were used: 

* Notion
* draw.io