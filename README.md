# Data Scientist

#### Technical Skills: Python + machine learning libraries (Pandas, Scikit-learn, Tensor Flow, Darts, etc.), R, SQL, MATLAB

### Education

#### Austral University (In progress)

Master in Data Science, expected date of completion December 2025.

#### University of Buenos Aires

Licenciado en ciencias matemáticas (Equivalent to M.Sc. in Mathematics), Math Science February 2018
Grade: 9.69

### Experience

**Data Scientist @ ITR (Oct 2024 - Present)**

- Development of machine learning and deep learning models, including time series predictive modeling and classification problems.
- Development of NLP applications using LLMs (chatbots, virtual assistants, multi-agent systems), including exploration of use cases and prototyping with RAG pipelines.
- Exploratory data analysis (EDA) and visualization for pattern identification and decision-making.

**Analyst Ssr @ Provincia Microcréditos (Apr 2024 - Oct 2024)**

- Process automation for granting micro-credit offers, integrating behavioral data and scores.
- Development and tuning of segmentation and prediction models to personalize offers and mitigate credit risk.
- Performance evaluation of campaigns and post-credit behavior, providing recommendations to optimize approval rates.

**Independent Consultant (Nov 2023 - Sept 2024)**

- Development of control systems based on time series.
- Development of machine learning models for churn prediction and automated candidate evaluation in recruitment processes.

**Data Analyst Ssr @ Puente Hermanos (Nov 2023 - Apr 2024)**

- Implementation of ETL processes integrating information from data warehouses, APIs, and other sources.
- Development of dashboards for data visualization and KPIs.
- Data analysis and insight generation for strategic decision-making.

**Data Science Tutor @ Coderhouse (Aug 2023 - Present)**

- Mentoring and technical review of practical projects in data science. Class instruction and assistance in machine learning, Python, and data analysis.

**Data Analyst & Scientist @ TIBEST Insurance Advisors (Feb 2023 - Sept 2023)**

- Data acquisition, ETL processes and automation. 
- Design, monitoring and presentation of dashboards and KPIs for data-based decision making.
- Customer segmentation and implementation in marketing campaigns.

**Doctoral researcher @ CONICET (Mar 2020 - Jan 2023)**

- Study and research in applications of mathematics and data science.

## Projects

### [Forecasting Interest Rate Spreads](https://github.com/HGalletti/Forecasting-Spread-Treasury-Bonds.git)

#### Project Purpose

This project focuses on the advanced analysis and forecasting of the **2Y-10Y interest rate differential** (spread), a critical macroeconomic indicator. The primary objective is to develop robust time series models to predict the future movements of this spread. A key aspect of this project involves strategically integrating other significant financial indicators, such as the VIX volatility index and the S&P 500 index, as exogenous variables to enhance the predictive accuracy and contextual relevance of the spread forecasts. This demonstrates proficiency in applying sophisticated statistical methodologies to real-world financial data.

#### Motivation

The 2Y-10Y interest rate spread is widely regarded as a leading indicator for economic cycles, recession probabilities, and market sentiment. Understanding and accurately forecasting its behavior is invaluable for investors, policymakers, and financial analysts. This project was motivated by the challenge of capturing the complex dynamics of this spread and exploring how its relationship with other major market indices can be leveraged for improved forecasting, highlighting a deep understanding of financial time series.

#### Technical Overview

The methodology employed in this project follows a comprehensive time series analysis pipeline:

-   **Exploratory Data Analysis (EDA):** Initial visualization and statistical analysis of the 2Y-10Y spread, VIX, and S&P 500 series to identify trends, seasonality, and volatility patterns. Cross-correlation analysis was performed to understand inter-dependencies.
-   **Data Preparation:** Handled missing values, applied necessary transformations (e.g., logarithmic) to stabilize variance, and performed stationarity tests (e.g., Augmented Dickey-Fuller) with appropriate differencing to prepare the data for modeling.
-   **Classic Time Series Modeling:** Implemented and optimized **ARIMA** (AutoRegressive Integrated Moving Average) and **SARIMA** (Seasonal ARIMA) models for the spread. Crucially, **SARIMAX** (Seasonal ARIMA with Exogenous Regressors) models were developed for the spread, incorporating the VIX and S&P 500 as exogenous variables to capture their influence.
-   **Model Validation and Evaluation:** Models were rigorously validated using train-test splits, and performance was assessed using standard metrics such as RMSE, MAE, and MAPE. Residual analysis was conducted to check model assumptions and identify areas for further improvement.

The project primarily utilizes Python with key libraries including `Pandas` and `NumPy` for data manipulation, `Matplotlib` and `Seaborn` for visualization, and `Statsmodels` for advanced time series modeling (ARIMA, SARIMA, SARIMAX).

#### Key Results

-   Successfully identified and addressed non-stationarity in the financial time series through appropriate differencing.
-   Developed **SARIMAX models** that effectively integrated the VIX and S&P 500 as exogenous variables, demonstrating improved predictive capabilities for the 2Y-10Y interest rate spread compared to univariate models.
-   The analysis of model residuals highlighted inherent complexities in financial data, such as heavy tails and heteroscedasticity, suggesting avenues for future exploration with more advanced modeling techniques.

[Project Link](https://github.com/HGalletti/Forecasting-Spread-Treasury-Bonds.git)

### [CV Assistant Chatbot](https://huggingface.co/spaces/HernanGalletti/CV_Hernan_Galletti)

#### Project Purpose

This project demonstrates an advanced Retrieval-Augmented Generation (RAG) system that serves as an interactive assistant for exploring my professional background, education, and skills. It showcases cutting-edge AI technologies including real-time multilingual processing, intelligent document retrieval, and conversation analytics, deployed as a production-ready application on Hugging Face Spaces.

#### Motivation

Traditional CVs lack interactivity and contextual depth. This chatbot transforms the career exploration experience, offering recruiters and collaborators an engaging, conversational way to discover relevant information while demonstrating practical implementation of enterprise-level AI systems.

#### Technical Overview

The system uses an advanced LangChain RAG pipeline with several key innovations:

- *Dynamic Multilingual System:* Real-time language switching between Spanish and English with native prompts (not translations) and complete conversational chain recreation
- *Balanced Diversified Retriever:* Two-stage filtering system that eliminates redundant content (>92% similarity) and ensures 3-6 diverse document sources per query, achieving 75% improvement over basic retrievers
- *Enterprise Logging:* Dual storage system with real-time Google Sheets logging and local backup, featuring UUID session tracking and comprehensive analytics
- *Advanced Vector Database:* ChromaDB with 26 unique chunks from 8 source documents, enriched with metadata for optimal retrieval

The system responds contextually in both languages, avoids hallucinations by grounding answers in embedded profile documents, and includes specialized prompts for professional tone and accuracy.

#### Deployment Features

- *Production Architecture:* Hosted on Hugging Face Spaces with error handling and <3 second response times
- *Interactive Gradio Interface:* Reactive components with complete UI translation and cultural context preservation
- *Conversation Analytics:* Anonymous session logging with Google Sheets API integration for usage pattern analysis
- *Optimized Performance:* ContextualCompressionRetriever with EmbeddingsRedundantFilter for maximum information diversity
- *Bilingual Knowledge Base:* Documents in Spanish and English with automatic language detection and source diversification

[Project Link](https://huggingface.co/spaces/HernanGalletti/CV_Hernan_Galletti)

### [Electoral Assistant](https://github.com/HGalletti/Asistente_electoral)

#### Project Objective

This project aims to develop a question-answering assistant that provides accurate and neutral responses about the 2025 legislative elections in Buenos Aires City (CABA), based on official documents and regulations.

#### Key Business Questions

- How can we ensure that electoral information is accessible, accurate, and up-to-date for citizens?
- What are the most common questions regarding voting procedures, registration, and polling logistics?
- How can generative AI and retrieval-based techniques be combined to deliver grounded, verifiable answers?
- What are the challenges of interpreting and summarizing legal electoral texts for general audiences?

#### Analytical Approach

The assistant uses a Retrieval-Augmented Generation (RAG) pipeline combining LangChain, OpenAI's language models, and a Chroma vector database. Official electoral documents are processed into text chunks and embedded into a vector store, enabling the assistant to retrieve relevant context when answering user queries. The system is optimized for clarity, neutrality, and traceability of responses, with a focus on document-based grounding and prompt engineering.

[Link](https://github.com/HGalletti/Asistente_electoral/blob/main/app.py)

---

*I'm currently working on new real-world data science projects and will be adding them here soon.*

## Some personal and older projects (Kaggle-based, 2022-2023)

These projects were developed as part of exploratory work and training, based on publicly available datasets from Kaggle. They involved full machine learning pipelines—from data exploration to model evaluation—and served as a foundation for further professional work in data science and machine learning.

### [SBA guaranted loans](https://github.com/HGalletti/SBA-Guaranteed-Loans/blob/main/Pr%C3%A9stamos%20garantizados%20por%20la%20SBA.pdf)

#### Project Introduction

In the realm of small business financing in the United States, the mission of the U.S. Small Business Administration (SBA) has been pivotal since its establishment in 1953. By promoting and supporting small enterprises within the U.S. credit market, the SBA has played a crucial role in fostering job creation and reducing unemployment.

One of the SBA's key initiatives is its loan guarantee program, designed to incentivize banks to extend loans to small businesses. Acting as an insurance provider, the SBA mitigates the risk for banks by guaranteeing a portion of the loan amount. In the event of a loan default, the SBA steps in to cover the guaranteed portion.

Despite SBA loans guaranteeing only a portion of the loan balance, banks still face the dilemma of whether to grant such loans, given the risk of default. Analyzing historical data becomes a valuable tool for informed decision-making in this context.

#### Project Objective

The primary business challenge is to determine if a loan can be granted with reasonable confidence that the borrowing company will repay it without significant issues.

#### Key Business Questions

- What defines companies that best predict loan repayment or potential problems?
- Does a company's history of multiple loans impact the likelihood of encountering repayment issues?
- How do the lending bank and credit line influence loan repayment?
- Is there a correlation between the loan term, the year the loan was issued, and repayment success?

#### Analytical Approach

Our objective is to develop a machine learning model that predicts whether a company may face difficulties in loan repayment, simplistically referred to as a "defaulted loan." This data science project involves a detailed exploratory data analysis (EDA) and is developed using technical tools like Python, Pandas, Scikit-learn, and more.

[Link](https://github.com/HGalletti/SBA-Guaranteed-Loans/blob/main/loans.ipynb)

### [Breast Cancer Detection](https://github.com/HGalletti/CancerDetection/)

#### Project Introduction

Breast cancer is a global health concern affecting millions of individuals every year. It's the second most common cancer in the world and poses a significant threat to women's health. Early detection plays a crucial role in improving survival rates and treatment outcomes.

#### Project Objective

The primary objective of this data science project is to develop a machine learning model that can accurately detect breast cancer based on parameters extracted from digitized images of breast masses. By analyzing these images, we aim to predict whether a mass is malignant or benign.

#### Key Business Questions

- What are the defining characteristics of tumors that best predict malignancy?
- How can machine learning assist medical professionals in making more accurate and timely diagnoses?
- What are the potential benefits and limitations of using automated image analysis in cancer detection?
- How can this technology contribute to early detection and improved treatment outcomes for breast cancer patients?

#### Analytical Approach

Our approach involves utilizing a diverse set of machine learning models, including logistic regression, decision trees, XGBoost, k-Nearest Neighbor, support vector machines, and a neural network. These models analyze features extracted from digitized images of breast masses. We employ Python, Pandas, Scikit-learn, TensorFlow, and other tools for data analysis, feature engineering, and model evaluation.

[Link](https://github.com/HGalletti/CancerDetection/blob/main/Cancer%20detection.ipynb)
