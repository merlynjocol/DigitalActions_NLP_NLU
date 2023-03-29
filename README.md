# Creating the Guidelines of Digital Actions for Social Impact. Combining Content Analysis, Text mining and Semantic Search

This repository is part of the HEIDI+ Project. 

The HEIDI project (Digital action at High Education institutions as a catalyst for social change) aspires to reposition HEIs with respect to society, as many traditional models of knowledge creation and circulation have shifted, challenged by bottom-up, community-driven action and the networking of individuals. 

The consortium is composed of partners with complementary profiles: 3 HEIs (University of Malta, University of Paris, and the University College London), one SME (W2L, Greece), and one NGO (CIP, Cyprus). Each partner has an intellectual output. The University of Paris has the responsibility to build a set of methodological guidelines for the design, implementation, and assessment of digital actions (materials needed, guidelines, tips, etc.), and the methodology for measuring the impact of Digital Actions (DA) awareness and training events, as well as the implementation of Digital actions.

In this project, the digital actions are the Citizen Science Project, the Maker Movement, and Hackathons/ Datathons.

## Objectives

Build the guidelines for digital actions using content analysis and text mining to gather information from stakeholder opinions, guidelines, scientific articles, and reports.

Specific objetives: 
- Collecting information from  the experience of the stakeholders in developing digital actions at the University of Paris, existing guidelines, scientific articles and reports
- Using content analysis and advance text mining to define the topics and gaps in methodologicla guidelines for digital actions


# Methods
The methodology follows the combination of content analysis, a qualitative analysis method working on
corpus from interviews and focus groups, and computational methods to mining scientific articles and
reports.


![methods](https://github.com/merlynjocol/DigitalActions_NLP_NLU/blob/b7775050f9de5b05469b0a651565d105eb89ee81/Images/Methods_heidi.png)


Bird Illustration source: James Brigs.
https://towardsdatascience.com/bert-for-measuring-text-similarity-eec91c6bf9e1



## Content analysis
The data used in the content analysis is not published in this repository for reasons of privacy and non  authorization to publish it.  The data came from interviews and focus groups. Label relevant words, phrases, sentences, or sections. Labels can be about actions, activities, concepts, differences, opinions, processes, or whatever you think is relevant.

This method combines theory-based coding with explorative coding to create a hybrid coding design. Therefore, the coding structure includes both theoretically and empirically driven units of analysis. The coding approach entails breaking down the text into its constituent parts by coding small parts of the larger text into categories. This typically involves a researcher or team of researchers developing a codebook, or dictionary, with which to categorize text. This process is iterative.



### Process

● Reading the transcripts

● Create and define labels. Definitions with clear meaning

● Decide on the coding strategy

● Label your research questions (code)

● search for relevant information in the data

● create and define labels


### Tools
Taguette is a free open-source text tagging tool for qualitative data analysis and qualitative research.


## Topic modelling (LDA) - Identification of Topics in Guidelines

Topic modeling is a probabilistic model that identifies topics covered in text. The technique used  is categorized as an unsupervised machine learning algorithm, Latent Dirichlet Allocation (LDA),  part of Python's Gensim package. 

### Process

- Collecting the documents

- Data cleaning

- Breakdown the documents into tokens

- Creation of Dictionary and Corpus

- Finding the optimal number of topics (LDA )


### Libraries

```
SpaCy
Seaborn
gesim
pyLDAvis 
pandas 

```


## Semantic Search 

Semantic similarity search is the task of searching for documents or sentences which contain semantically similar content to a user-submitted search term. This task is often carried out, for instance when searching for information on the internet. To facilitate this, vector representations referred to as embeddings of both the documents to be searched as well as the search term must be created. 

The approaches include neural networks, which have seen a large rise in popularity over the last few years. The BERT network released in 2018 is a highly regarded neural network which can be used to create embeddings. Multiple variations of the BERT network have been created since its release, such as the
Sentence-BERT network which is explicitly designed to create sentence embeddings.

The idea behind semantic search is to embed all entries in your corpus, whether they be sentences, paragraphs, or documents, into a vector space. At search time, the query is embedded into the same vector space and the closest embeddings from your corpus are found. 

### Process 

- Create the corpus from scientific publications and reports from different organizations

- Work with the text from the Discussions and Conclusions part of scientific article. For the papers which don’t
have a discussion part, I take only the conclusions.

- Break the text by sentences (Sentence Segmentation)

- Create a list of this sentences in the document

- Download the models to compare

- Encoder the dataset and the query

- Apply the Cosine similarity between the query and sentences of the corpus


### Libraries
```
SpaCy
pySBD
S-BERT
numpy
pandas

```

### Pre-trained models
Pre-models developed by UKLab and Allen institute, in the repository of Hugging Face Transformers

```
- model 1: Original model
  model1 = SentenceTransformer('bert-base-nli-mean-tokens')

- model 2:
  Model2 SentenceTransformer('sentence-transformers/multi-qa-MiniLM-L6-cos-v1')

- model 3: SciBERT
 model3 = SentenceTransformer('allenai/scibert_scivocab_uncased')
 
```

# Licensing

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Credits

Many thanks to [HEIDI+ Project][(https://github.com/pierrepo](https://heidiproject.eu/)
