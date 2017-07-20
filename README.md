# Microsoft-70-774-ExamPrep
Perform Cloud Data Science with Azure Machine Learning

https://buildazure.com/2017/02/09/70-774-perform-cloud-data-science-with-azure-machine-learning-certification-exam/

## Prepare Data for Analysis in Azure Machine Learning and Export from Azure Machine Learning
  + **Import and export data to and from Azure Machine Learning.** Import and export data to and from Azure Blob storage, import and export data to and from Azure SQL Database, import and export data via Hive Queries, import data from a website, import data from on-premises SQL
    - Import from file by clicking `New` in bottom left corner
    - Import from the other sources `Data Input and Output -> Import Data`
    - Export using `Data Input and Output -> Export Data`
      
  + **Explore and summarize data.**  Create univariate summaries, create multivariate summaries, visualize univariate distributions, use existing Microsoft R or Python notebooks for custom summaries and custom visualizations, use zip archives to import external packages for R or Python
    + Univariate/Multivariate Statistics and Visualizations
       - 1: Click on the output connector below the data set.
       - 2: Select `Visualize`.  This will bring up a helpful screen which includes:
          + A view of the dataset.
          + A histogram (or boxplot, your choice) for numeric variables
          + A bar chart for categorical variables
       - 3: Select a column by clicking anywhere in the column itself.  This activates the `Statistics` and `Visualizations` options on the right.
          + Statistics (for categorical values, only last three provided)
            + Mean
            + Median
            + Min
            + Max
            + Standard Deviation
            + Unique Values
            + Missing Values
            + Variable Type
          + Visualizations
            + Bar Chart for Categorical (can log scale)
            + Histogram
              - log scale x or y
              - change bin number
              - overlay cum dist or prob dens
            + Box Plot (can log scale)
        - 4:  Under `compare to` drop down, select another variable for multivariate analysis
          + If 2 quantitative variables, scatterplot shown (can log scale)
          + If 2 categorical variables, cross tabulation shown (table of frequencies)
          + If 1 categorical and 1 quantitative, then side-by-side boxplots shown
        - 5: Can also use the `Summarize Data` module to get additional insight (kurtosis, percentiles, variance, range)
          
    + Notebooks 
      - Can explore a data set in an existing notebook by simply opening the notebook on the left side
      - Can create a new notebook to explore the data set by clicking on the output connector below data set, and select `Open in a new Notebook`
    + R - Under `R Language Modules` drag `Execute R Script` onto workspace
      + Select data input(s) and connect to R node
      + Can also connect a zipped package as a dataset, and install via R script
    + Python - Under `Python Language Models` drag `Execute Python Script` onto workspace
      + Use `azureml_main` function to connect one or two datasets into Python node
      + Use third input port to bring in zipped script bundle `Import mymodule`
      
  + **Cleanse data for Azure Machine Learning.**  Apply filters to limit a dataset to the desired rows, identify and address missing data, identify and address outliers, remove columns and rows of datasets
    + Filter
      - `Split Data` and use regular or relative expression
      - `Apply SQL Transformation` - can use this to filter rows
    + Missing Data
      - `Clean Missing Data` node can be used to address issues of missing data
      - Select which columns to clean
      - Choose Cleaning Mode (Mean, Median, Mode, PCA, Custom, Remove row/column, MICE)
    + Outliers
      - `Clip Values` can define constant or percentage to clip peaks or subpeaks(or both)
      - Replace with mean, median, threshold, or missing
      - Add indicator column to see if value was clipped
    + Remove Columns and Rows
      - `Select Columns`
      - `Remove Duplicate Rows`
    
  + **Perform feature engineering** Merge multiple datasets by rows or columns into a single dataset by columns, merge multiple datasets by rows or columns into a single dataset by rows, add columns that are combinations of other columns, manually select and construct features for model estimation, automatically select and construct features for model estimation, reduce dimensions of data through principal component analysis (PCA), manage variable metadata, select standardized variables based on planned analysis
    + Merge
      - `Join Data` connect two datasets to join
      - Select key column(s) for both datasets
      - Match case?
      - Type of join?
    + Feature Selection
    + PCA
    + Variable Metadata
    + Standardized Variables
    
## Develop Machine Learning Models
  + Select an appropriate algorithm or method
    + Select an appropriate algorithm for predicting continuous label data, select an appropriate algorithm for supervised versus unsupervised scenarios, identify when to select R versus Python notebooks, identify an appropriate algorithm for grouping unlabeled data, identify an appropriate algorithm for classifying label data, select an appropriate ensemble
  + Initialize and train appropriate models
    + Tune hyperparameters manually; tune hyperparameters automatically; split data into training and testing datasets, including using routines for cross-validation; build an ensemble using the stacking method
  + Validate models
    + Score and evaluate models, select appropriate evaluation metrics for clustering, select appropriate evaluation metrics for classification, select appropriate evaluation metrics for regression, use evaluation metrics to choose between Machine Learning models, compare ensemble metrics against base models

## Operationalize and Manage Azure Machine Learning Services
  + Deploy models using Azure Machine Learning
    + Publish a model developed inside Azure Machine Learning, publish an externally developed scoring function using an Azure Machine Learning package, use web service parameters, create and publish a recommendation model, create and publish a language understanding model
  + Manage Azure Machine Learning projects and workspaces
    + Create projects and experiments, add assets to a project, create new workspaces, invite users to a workspace, switch between different workspaces, create a Jupyter notebook that references an intermediate dataset
  + Consume Azure Machine Learning models
    + Connect to a published Machine Learning web service, consume a published Machine Learning model programmatically using a batch execution service, consume a published Machine Learning model programmatically using a request response service, interact with a published Machine Learning model using Microsoft Excel, publish models to the marketplace
  + Consume exemplar Cognitive Services APIs
    + Consume Vision APIs to process images, consume Language APIs to process text, consume Knowledge APIs to create recommendations

## Use Other Services for Machine Learning
  + Build and use neural networks with the Microsoft Cognitive Toolkit
    + Use N-series VMs for GPU acceleration, build and train a three-layer feed forward neural network, determine when to implement a neural network
  + Streamline development by using existing resources
    + Clone template experiments from Cortana Intelligence Gallery, use Cortana Intelligence Quick Start to deploy resources, use a data science VM for streamlined development
  + Perform data sciences at scale by using HDInsights
    + Deploy the appropriate type of HDI cluster, perform exploratory data analysis by using Spark SQL, build and use Machine Learning models with Spark on HDI, build and use Machine Learning models using MapReduce, build and use Machine Learning models using Microsoft R Server
  + Perform database analytics by using SQL Server R Services on Azure
    + Deploy a SQL Server 2016 Azure VM, configure SQL Server to allow execution of R scripts, execute R scripts inside T-SQL statements
