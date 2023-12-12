# Optimizing Political Analysis: Advanced Integration of LangChain with LLMs

## Team Members: Yixuan Zhang, Haoyu Fu

<div style="display: flex; justify-content: center;">
  <a href="https://youtu.be/UppUEKHn50c">
    <img src="https://res.cloudinary.com/marcomontalbano/image/upload/v1702203551/video_to_markdown/images/youtube--UppUEKHn50c-c05b58ac6eb4c4700831b2b3070cd403.jpg" alt="Elevator Pitch For Optimizing Political Analysis: Advanced Integration of LangChain with LLMs" width="500" height="300">
  </a>
</div>

## Project Description
The objective of this project is to explore the possibility of using Large Language Models to make predictions on political stances of users from social medias. Currently we are specifically working on using Twitter data collected during the 2020 US Presidential Election with OpenAI models.

## Files

```
Optimizing-Political-Analysis-Advanced-Integration-of-LangChain-with-LLMs/
├── data/                               # Data directory containing datasets, generated responses, etc.
│   ├── hashtag_joebiden.csv                    # raw dataset 1
│   ├── hashtag_donaldtrump.csv                 # raw dataset 2
│   ├── cleaned_tweets_biden.csv                # cleaned dataset 1
│   ├── cleaned_tweets_trump.csv                # cleaned dataset 2
│   └── in_context_responses.csv                # generated responses
├── documents/                         # Written reports and future plans
│   ├── DSC_180A_Quarter_1_Project_Report.pdf
│   ├── DSC_180A_Quarter_2_Project_Proposal.pdf
│   └── DSC_180A_Quarter_2_Project_Schedule.pdf
├── data_cleaning.ipynb                # Jupyter notebook for raw data cleaning
├── demo.ipynb                         # Jupyter notebook for generating reponses
├── keys_config.py                     # Config file for storing API keys
├── prompting.py                       # Scripts for generating prompts and querying responses
├── tools.py                           # Scripts for data processing and visualizations
├── visualization_overview.ipynb       # Jupyter notebook for overview visualizations
└── visualizations_bias.ipynb          # Jupyter notebook for bias visualizations
```

## Installation and Reproduction Instructions
The following instructions show the steps to reproduce the results of our report. 
1. **Setting up Environment**: run the following command to install packages used in our project: ```pip install regex pandas openai seaborn matplotlib langchain``` 

2. **Downloading the raw data**: Download the [raw data](https://www.kaggle.com/datasets/manchunhui/us-election-2020-tweets/). Make sure the two files `hashtag_donaldtrump.csv` and `hashtag_joebiden.csv` are located under `/data` directory.

3. **Data Cleaning**: Run all the cells from `data_cleaning.ipynb`. The results will be saved in `/data` directory.

4. **API keys**: An OpenAI API key is required to run our code. Go to the [OpenAI website](https://platform.openai.com/api-keys) to get a key. Open the `keys_config.py` file and replace the value of `openai.api_key` by the string of your API key.

5. **Generating responses**: Run all the cells from `demo.ipynb` to generate simulated responses from LLMs. The results will be processed and saved in `/data/in_context_responses.csv`. Note that the runtime can be greater than 10 minutes due to the large data size.

6. **Visualizing**: Run `visualization_overview.ipynb` and `visualizations_bias.ipynb` to check the final visualizations and results of our project report. Note that the runtime can be greater than 10 minutes due to the large data size.
