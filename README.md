# Knowledge Graphs Based Data Science Pipeline

## Overview

This project is focused on enhancing traditional data science pipelines by leveraging knowledge graphs. The aim is to create an end-to-end data science pipeline that includes data collection, preprocessing, and advanced analysis using knowledge graphs (KGs). This README provides an overview of the datasets, preprocessing steps, and the tools used.

## Project Structure

- **Data**: Contains the raw datasets.
  - `authors_final.csv`
  - `genres_pages_x_books.csv`
  - `interactions_final.csv`
  - `filtered_books.csv`
- **Preprocessing**: Contains the notebook for data preprocessing.
  - `preprocessing.ipynb`

## Datasets

### 1. `authors_final.csv`
Contains information about the authors.

| Column Name | Description |
|---|---|
| author_id | Unique identifier for the author. |
| name | Name of the author. |
| average_rating | Average rating of the author's books. |
| ratings_count | Number of ratings received by the author's books. |

### 2. `genres_pages_x_books.csv`
Links books to their genres and number of pages.

| Column Name | Description |
|---|---|
| book_id | Unique identifier for the book. |
| `<genre>` | A variable for each genre which represents the probability of the book belonging to it. |
| num_pages | Number of pages the book has. |

### 3. `interactions_final.csv`
Contains user interactions with the books.

| Column Name | Description |
|---|---|
| user_id | Unique identifier for the user. |
| book_id | Unique identifier for the book. |
| is_read | Whether the user has read the book (1 if read, 0 otherwise). |
| rating | Rating given by the user. |
| is_reviewed | Whether the user has reviewed the book (1 if reviewed, 0 otherwise). |

### 4. `filtered_books.csv` 
Contains information about the books.

| Column Name | Description |
|---|---|
| book_id | Unique identifier for the book. |
| writers | List of author identifiers who have writen the book. |
| illustrators | List of author identifiers who have illustrated the book. |
| contributors | List of author identifiers who have contributed to the book. |
| editors | List of author identifiers who have edited the book. |
| translators | List of author identifiers who have translated the book. |
| similar_books | List of similar books by identifier. |  
| publication_year | String defining the year the book was published. |
| title | Title of the book. |


## Preprocessing

The preprocessing step involves cleaning and preparing the data for analysis. The `preprocessing.ipynb` notebook includes the following steps:

1. **Loading Data**: Load datasets from CSV files.
2. **Data Cleaning**: Handle missing values, incorrect data types, and duplicates.
3. **Filtering**: Filter interactions to include only unread books (`is_read == 0`).
4. **Sampling**: Get a sample of books and users to reduce the dataset.

## Knowledge Graphs

The next phase involves converting the preprocessed data into knowledge graphs. We will use RDFLib for modeling and SPARQL for querying the graphs. The key steps are:

- **Modeling the Graph:** Define the schema and relationships.
- **Loading Data into the Graph:** Populate the graph with data from the trusted zone.
- **Querying the Graph:** Use SPARQL to extract insights and perform analysis.

### Tools and Technologies

- **Python:** Main programming language.
- **RDFLib:** Library for working with RDF (Resource Description Framework) data.
- **SPARQL:** Query language for RDF.
- **Jupyter Notebook:** For interactive data processing and analysis.
- **GraphDB:** For storing and querying knowledge graphs.
- **PyTorch:** For machine learning tasks using graph embeddings.
- **Scikit-Learn:** For additional machine learning tasks.

### Future Work

- **Graph Embeddings:** Generate embeddings from the knowledge graph and apply machine learning algorithms.
- **Comparative Analysis:** Compare the performance of traditional models with KG-based models.
- **Advanced Queries:** Implement complex SPARQL queries to extract more nuanced insights.

### Conclusion

This project aims to demonstrate the power of knowledge graphs in enhancing data science pipelines by providing a structured and semantically enriched approach to data analysis. Stay tuned for updates on the implementation of knowledge graph embeddings and advanced analytical techniques.



