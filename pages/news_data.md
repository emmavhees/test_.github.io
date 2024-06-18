# Using Bing News API and ChatGPT for Updating Potential Customer Information in Salesforce 
<!-- Automating Marketing Task / Operational efficiency -->

##  Task Overview
The tasks consists of finding companies who have recently made some kind of climate commitment such as  100% renewable or a net-zero target.

## Challenge
This task is done manually and is very time intesive and repetitive. Is there a way of automating this task in order to save time (operational effiency).

## Initial Solution
Google alerts are set on a list of keywords in several languages and every week the resulting emails are checked. This consists of clicking on every link, checking the (news)article and determining if it is relevant or not. If yes then additionally some data points need to be extracted and entered in Salesforce (CRM system). 

### Issues
- labour intensive
- time intensive

## Improved Solution
### New Solution
- Utilize [Bings News API](https://azuremarketplace.microsoft.com/en-us/marketplace/apps/microsoft.bingsearch?tab=overview) to receive news articles based on different keywords and in different regions.
- Leverage ChatGPT for determining relevance of the articles and extracting the neccessary datapoints. 
- Run this pipeline on Google Cloud Platform on a set schedule. 

### Approach

- Create 2 separate modules; one for the retrieving the articles and one for reviewing them. 
- News module: retrieve articles using Bing news API and store the found articles on Google Bigquery
- ChatGPT Prompt engineerding: break up the task that need to be performed by ChatGPT: 
    1. Determine relevance 
    2. Extract datapoints
    3. Translate (depending on the language) and return summary
- Reviewing module: 
    1. Retrieve data from Google Bigquery
    2. Process data using the steps above
    3. Load transformed data to Google Bigquery
    4. Ingest extracted datapoints to Salesforce 

## Addressing Key Issues

### Labour
With the new solution, the individual now only needs to check one document, eliminating the need to click through multiple links and articles to find the necessary information. This document contains the datapoints that were extracted and uploaded to Salesforce.

### Time
The individual previously in charge of this task reported spending about 4 hours weekly on it. After implementing the new solution, they now spend only around 30 minutes per week. This significant time reduction greatly enhances operational efficiency.

## Solution Diagram
![News Data ](..\images\news_diagram.png)

<!-- 100% privacy-first analytics -->
<script async defer src="https://scripts.simpleanalyticscdn.com/latest.js"></script>
<noscript><img src="https://queue.simpleanalyticscdn.com/noscript.gif" alt="" referrerpolicy="no-referrer-when-downgrade" /></noscript>