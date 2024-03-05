# Aegean-Employment-Scams-Detection-App
AI-powered classifier mobile app using NLP to spot fake job ads and protect users from online scams. Our system analyzes language patterns and leverages algorithms to create a safe and trustworthy job search experience.

In today's competitive job market, sifting through countless online job postings can be overwhelming. Sadly, among legitimate opportunities, insidious employment scams lurk, putting job seekers at risk of financial loss and identity theft. This project addresses this critical issue by empowering job seekers with an AI-powered classifier built using Machine Learning and Natural Language Processing (NLP). Our innovative system aims to accurately distinguish between genuine and fraudulent job advertisements, shielding users from deceptive tactics. By analyzing linguistic patterns and leveraging advanced algorithms, we strive to create a secure and trustworthy online job search experience, ultimately protecting individuals from falling victim to malicious schemes.

### Dataset
- Origin: University of the Aegean
- Rows: 17,880

### Synthetic Dataset
- Source: Gretel.ai
- Rows: 5000

### Initial Data Analysis

- Education Level

The dataset encompasses a broad range of educational qualifications, from Bachelor's Degrees to vocational certifications. An intriguing pattern emerged during the analysis of education data: despite similar educational requirements, job listings often had distinct labels. For instance, some required a "Bachelor's Degree," while others opted for "Bachelor's or Equivalent." This disparity underscores the need for meticulous data cleaning and mapping to standardize similar qualifications for accurate analysis and model training.

- Industry Level
The dataset spans various industries, with Information Technology and Services emerging as dominant (11.3% of postings). The top 10 industries are highlighted, with others categorized under "Others" for clarity.

### Data Cleaning and Preprocessing Overview

Data Cleaning:

- Data Augmentation: Integrated synthetic data to enhance diversity and volume.
- Handling Null Values: Replaced with 'Unspecified,' retaining NaN in specific columns.
- Mapping Education Level: Custom function to standardize labels.
- Location Standardization: Extracted two-character country codes for consistency.
- Industry Mapping: Reorganized industries based on common traits.
- Number to Text Transformation: Binary values mapped to descriptive labels.
- Merging Text Columns: Consolidated text columns into 'full_text' for efficiency.

Text Processing:

- Tokenization: Segmenting full text into words.
- Lowercasing: Ensuring consistency.
- Removal of Non-Alphabetic Characters: Filtering out non-alphabetic characters.
- Stop Word Removal: Eliminating common English stop words.
- Lemmatization: Words reduced to base form for consistency.
- Part-of-Speech Tagging: Assigning grammatical categories.
- Detokenization: Reconstructing preprocessed tokens into coherent text.

### Improved Data Representation
Vectorization methods such as TF-IDF, Count Vectorization, word2vec, and BERT converted text into numerical vectors, capturing semantic relationships for improved representation.

### Exploratory Data Analysis (EDA)

Employment Type
- Full-time: 14,931 entries
- Contract: 1,762
- Part-time: 1,054
- Other: 308
- Temporary: 266

Locations (Country)
- United States: 64% of job postings
- Great Britain: 10.5%

Industries
- Before Cleaning: Various categories lacking uniformity.
- After Cleaning: Reorganized into broader groups for clarity.

Educational Qualifications
- Before Cleaning: Diverse range of qualifications.
- After Cleaning: Standardized into broader categories.

Experience
- Mid-Senior Level: 4,307 occurrences
- Entry Level: 4,130

Numerical Features Correlation Analysis
- Job ID: Moderate positive correlation (0.38) with fraudulence.
- Company Logos: Significant negative correlation (-0.56) with fraudulence.
- Questions in Postings: Moderate negative correlation (-0.27) with fraudulence.

Bigram Analysis
- Revealed linguistic patterns in genuine and deceptive job postings.

Industry Disparities
- Different landscape between real and fake job postings, with energy leading in fake postings.

Education Requirements
- Bachelor's degree most common in fake postings, while unspecified qualifications prevalent.

### Splitting Data into Train-Test
- Utilized train_test_split function with a test size of 40%.

### Modeling and Vectorization
- Techniques: TF-IDF, Count Vectorization, word2vec, BERT
- Models: Naive Bayes, Random Forest, SVM, RNN, LSTM

### Conclusion
- Models achieved accuracies between 97% and 98%.
- RNN and LSTM models demonstrated superior performance, achieving 99% accuracy.
- These models offer better generalization to unseen data and are less prone to overfitting, enhancing scam detection capabilities.

This project aims to combat employment scams by empowering users with an AI-powered classifier, creating a safe and reliable job search environment.





