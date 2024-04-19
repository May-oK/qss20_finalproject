# qss20_finalproject

## Group members: Khine, Lekina, Robang

## Project option: Option 3. Text Analysis and Uncovering Demographic or Regional Differences in Family Caregiver Experiences

### Description
For our project, we performed a text analysis to uncover demographic differences in family caregiver experiences. We set out to identify themes, commonalities, and changes across different demographics based on the open-ended responses in the FEIS survey. By analyzing variation between demographic groups, we were hoping to determine if and how peoples' needs and opinions of mental health services changed and whether their requests were met, or the suggestions they made had been heard during the pandemic.

### Questions of interest
1. What keywords and themes are most prevalent in responses from individuals with IDD and their families highlighting still-standing mental health needs and services?
2. How do they vary with racial groups, gender, and nature of disability?


### Data
1. START Family Experience Interview Survey (FEIS) - tracks the responses of participants with START activity and their evaluation of mental health services. Emphasis was placed on the last two open-ended questions:
   * ...any particular service that your family member needed that was not available?
   * What advice would you give to service planners regarding the mental health service needs of persons with IDD and their families?

2. Dartmouth Dataset - contains all START services that occurred during the relevant time period.

Data files protected. 

### Code
1. `01_topic_modeling.ipynb`
   * Input: START Family Experience Interview Survey (FEIS) dataset
   * Purpose: Subsets to the relevant open-response columns and constructs an topic model for said columns.
   * Output: An optimized LDA topic model to be used in estimating topics and their respective significant words.

2. `02_visualization.ipynb`
   * Input: START Family Experience Interview Survey (FEIS) and Dartmouth Datasets
   * Purpose: Merges relevant columns in both datasets and categorizes the responses by demographics. The LDA model is then used to estimate topics and top words for each category and visualize the results.
   * Output: A series of pyLDAvis plots and .csv files for each category.

Code samples linked [here](code/).



### Output
The aforementioned pyLDAvis plots and .csv files that capture the topic model's implementation on the open-ended responses.

```
output
├── presentation_slides
│   └── qss20_finalslides.pdf
└── topic_model_vis
    ├── response_advice
    │   ├── by_demographic
    │   │   ├── Gender
    │   │   │   ├── model_Female.csv
    │   │   │   ├── model_Female.html
    │   │   │   ├── model_Male.csv
    │   │   │   └── model_Male.html
    │   │   ├── Level\ of\ Intellectual\ Disability
    │   │   │   ├── model_Mild.csv
    │   │   │   ├── model_Mild.html
    │   │   │   ├── model_Moderate.csv
    │   │   │   ├── model_Moderate.html
    │   │   │   ├── model_Severe.csv
    │   │   │   └── model_Severe.html
    │   │   └── Race
    │   │       ├── model_White.csv
    │   │       ├── model_White.html
    │   │       ├── model_not_White.csv
    │   │       └── model_not_White.html
    │   └── whole_corpus
    │       ├── model_response_advice.csv
    │       └── model_response_advice.html
    └── response_service
        ├── by_demographic
        │   ├── Gender
        │   │   ├── model_Female.csv
        │   │   ├── model_Female.html
        │   │   ├── model_Male.csv
        │   │   └── model_Male.html
        │   ├── Level\ of\ Intellectual\ Disability
        │   │   ├── model_Mild.csv
        │   │   ├── model_Mild.html
        │   │   ├── model_Moderate.csv
        │   │   ├── model_Moderate.html
        │   │   ├── model_Severe.csv
        │   │   └── model_Severe.html
        │   └── Race
        │       ├── model_White.csv
        │       ├── model_White.html
        │       ├── model_not_White.csv
        │       └── model_not_White.html
        └── whole_corpus
            ├── model_response_service.csv
            └── model_response_service.html

14 directories, 33 files
```

Graphs and figures linked [here](output/).
