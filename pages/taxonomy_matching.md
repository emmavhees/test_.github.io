# Product Categorization for CO2 Emission Compensation

## Product Overview
A Shopify plugin that enables customers to compensate for the CO2 emissions of their purchases.

## Challenge
Determining the Google taxonomy of a product is difficult due to the vast number of products and the range in product names.

## Initial Solution
- Feeding a list of Google taxonomies to ChatGPT (OpenAI).
- Asking the model to categorize a list of products based on these taxonomies.

### Issues
- Lack of explainability
- High cost
- Seemingly low accuracy

## Improved Solution

### New Solution
- Utilize an open-source sentence similarity model to calculate similarity scores between taxonomy descriptions and product names.
- Return the top 3 most similar taxonomies along with their scores.

### Approach
- Test various open-source sentence similarity model encoders to identify the most accurate one for our problem.
- Encode all Google taxonomies up to level 4 and store them in cloud storage.
- Develop a calculation module to encode product names, retrieve taxonomy encodings, calculate cosine similarity, and return the top N highest scoring taxonomies.
- Create a test set by scraping Google Shopping to evaluate the accuracy of both current and new solutions.
- Deploy an API service to enable batch processing of product names.

## Addressing Key Issues

### Explainability
With the cosine similarity metric, we can now transparently explain why a product name is matched to a taxonomy, improving the overall clarity of the solution.

### Cost
The cost associated with our solution primarily stems from the resource use of the API, which is significantly lower compared to using OpenAI's API, ensuring cost-effectiveness.

### Accuracy
Leveraging our newly created test set, we measured the accuracy for both the previous and new models. The new model yields an accuracy rate of approximately 97%, compared to the previous solution's accuracy of around 54%, demonstrating substantial improvement.

### Solution diagram

![Taxononmy matching ](..\images\taxonomy_matching.png)