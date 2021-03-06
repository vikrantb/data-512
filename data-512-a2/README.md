# Bias in Data

## Goal
The goal of this project is to identify what, if any, sources of bias may exist in various Wikipedia talk corpus datasets, and to develop testable hypotheses about how these biases might impact the behavior of machine learning models trained on the data, when those models are used for research purposes or to power data-driven applications. 

Google data scientists used these [annotated datasets](https://figshare.com/projects/Wikipedia_Talk/16731) to train machine learning models as part of a project called Conversation AI. The models have been used in a variety of software products and made freely accessible to anyone through the Perspective API. 

As part of this assignment project, we want to study these datasets and try to identify potential biases or potential unintended negative consequences.

## Data Citations

To use the data, we needed to use
1. Figshare datasets specifically for aggressiveness in text and toxicity. Which can be found [here](https://figshare.com/projects/Wikipedia_Talk/16731)
2. The [Detox wiki page](https://meta.wikimedia.org/wiki/Research:Detox)
3. [Perspective API repository](https://www.perspectiveapi.com/#/home) - wiki page [here](https://github.com/conversationai/perspectiveapi/blob/master/2-api/methods.md)
4. Google [Coversation AI project](https://conversationai.github.io/)
## Data description
Detailed data description can be found [here](https://meta.wikimedia.org/wiki/Research:Detox/Data_Release)

## Notebook used in analysis
[This](https://github.com/vikrantb/data-512/blob/main/data-512-a2/hcds-a2-data-bias.ipynb) is the notebook that we used for analysis.
[This](https://github.com/vikrantb/data-512/tree/main/data-512-a2/images) is where the images required for analysis are saved. Although, they can be found directly inline in the notebook.
