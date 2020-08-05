# 2k18-csee-28

Title: 
     “AIMMX: Artificial Intelligence Model Metadata Extractor”
Author:
Jason Tsay, IBM Research, Yorktown Heights, New York, USA
Alan Braz IBM Research, Sao Paulo, Brazil
Martin Hirzel, Avraham Shinnar, Todd Mummert, IBM Research, Yorktown Heights, New York, USA

Conference Name: 
         2020 International Conference on Software Engineering
Introduction and motivation:
                     Despite all of the facility that machine learning and AI (AI) models bring back applications, much of AI development is currently a reasonably unplanned process. Software engineering and AI Development share many of an equivalent languages and tools, but AI development as an engineering practice remains in early stages. Mining. Software repositories of AI models enables insight into the present State of AI development. However, much of the relevant metadata around models aren't easily extractable directly from repositories And require deduction or domain knowledge. This paper presents a Library called AIMMX that permits simplified AI Model Metadata Extraction from software repositories. The combination of sufficient hardware resources, the supply of large amounts of knowledge, and innovations in AI (AI) models has caused a renaissance in AI research and practice. For this paper, we define an AI model as all the software and data artifacts needed to define the statistical model for a given Task, train the weights of the statistical model, and/or deploy the trained model weights for prediction during a service or application. Our definition of model includes both traditional machine learning (ML) and deep learning models. AI as an engineering practice is still in its early stages with often unpredictable and dear results (Both in terms of your time and quality) which are often difficult to reproduce. The sheer amount of possible AI approaches and Algorithms and up to date increase in released AI frameworks Result in an outsized sort of AI models and representations. The Sheer variety and lack of standardization leads to models that are Difficult to interact with and reason across at scale.

Research Methodology:

![](images/filename%20dann.png)

This paper makes the following contributions:
Tool for extracting AI model-specific metadata from software Repositories with currently five extraction modules (Section 2).
Evaluation of our tools against a dataset of 7,998 models (Section 3). This AI model metadata dataset is also available as part of a replication package.
Preliminary usage of extracted metadata via an exploratory Analysis of the data and method reproducibility of AI models in our dataset and implementation of a cataloging tool (Section 4).

AUTOMATED MODEL METADATA EXTRACTION:
            The core of AIMMX is a Python library that reads software repositories, specifically from GitHub, and extracts AI model-related information into standardized model metadata in the JSON format that is machine and human readable. This library is open source and publicly available for use1. AIMMX is meant to be simple to use: once it is instantiated with a GitHub API key, then the user calls a function with a desired GitHub URL which then runs the extractors and returns the extracted metadata. The advantages of choosing to use software repositories and GitHub specifically are that they are already in common use for AI development.

Model Name Extraction
Reference Extraction
Dataset Extraction
AI Framework Extraction
Automated Domain Inference


Evaluation and Preliminary  Analysis:

Evaluation Dataset
Model Name Extraction
Reference Extraction
Dataset Extraction 
Frame Extraction 
Automated Domain Inference
System Evaluation


PRELIMINARY METADATA USAGE:
Exploratory Reproducibility Analysis
Model Catalog Tool

Threats of Validity

RELATEDWORK

Software and AI Development
Model Metadata Mining and Inference
Model Catalogs


CONCLUSIONS:

This paper describes AIMMX which we intend as a step towards furthering engineering support for AI development through providing standardized metadata for existing AI models. We envision that generating analyzable metadata for disparate models is both the first step towards managing models at scale and adapting existing mining software repositories techniques to AI models.
