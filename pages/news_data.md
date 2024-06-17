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
- Utilize Bings News API (add link) to receive news articles based on different keywords and in different regions.
- Utilize (find synonym) ChatGPT for determining relevance of the articles and extracting the neccessary datapoints. 
- Run this pipeline on Google Cloud Platform on a set schedule. 

### Approach

- Create 2 separate modules; one for the retrieving the articles and one for transforming (ander woord) them. 
- News module will retrieve articles using Bing news API and store the found articles on Google Bigquery
- Break up task that need to be performed by ChatGPT: 
    1. Determine relevance 
    2. Extract datapoints
    3. Translate (depending on the language) and return summary

## TBC