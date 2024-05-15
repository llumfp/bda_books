# Knowledge Graphs Based Data Science Pipeline

## Overview

This project is focused on enhancing traditional data science pipelines by leveraging knowledge graphs. The aim is to create an end-to-end data science pipeline that includes data collection, preprocessing, and advanced analysis using knowledge graphs (KGs). This README provides an overview of the datasets, preprocessing steps, and the tools used.

## Project Structure

- **Data**: Contains the raw datasets.
  - `authors.csv`
  - `genres_pages_x_books.csv`
  - `interactions_sample.csv`
- **Preprocessing**: Contains the notebook for data preprocessing.
  - `preprocessing.ipynb`

## Datasets

### 1. `authors.csv`
Contains information about the authors.
- `author_id`: Unique identifier for the author.
- `name`: Name of the author.
- `average_rating`: Average rating of the author's books.
- `rating_counts`: Number of ratings received by the author's books.

### 2. `genres_pages_x_books.csv`
Links books to their genres and includes additional information.
- `book_id`: Unique identifier for the book.
- `authors`: Authors of the book.
- `similar_books`: List of similar books.
- `publication_year`: Year the book was published.
- `title`: Title of the book.

### 3. `interactions_sample.csv`
Contains user interactions with the books.
- `user_id`: Unique identifier for the user.
- `book_id`: Unique identifier for the book.
- `is_read`: Whether the user has read the book (1 if read, 0 otherwise).
- `rating`: Rating given by the user.

## Preprocessing

The preprocessing step involves cleaning and preparing the data for analysis. The `preprocessing.ipynb` notebook includes the following steps:

1. **Loading Data**: Load datasets from CSV files.
2. **Data Cleaning**: Handle missing values, incorrect data types, and duplicates.
3. **Filtering**: Filter interactions to include only unread books (`is_read == 0`).

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
