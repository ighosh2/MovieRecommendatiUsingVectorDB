# Movie Recommendation System Using Vector Databases

## Project Overview
This project demonstrates the implementation of a **movie recommendation system** using **vector embeddings** and a **vector database (Pinecone)**. The system leverages machine learning models for generating embeddings from movie descriptions and performs similarity searches to recommend movies based on a user's query.

## Features
- **Data Preparation:** Processes and refines a dataset of movies, including their titles, genres, IMDB ratings, and descriptions.
- **Embedding Generation:** Utilizes the pre-trained `SentenceTransformer` model (`all-MiniLM-L6-v2`) to encode movie descriptions into numerical vectors.
- **Vector Database Integration:** Stores the embeddings in Pinecone, a cloud-based vector database, along with metadata for each movie.
- **Querying for Recommendations:** Accepts a natural language query from the user and retrieves the top similar movies based on embedding similarity.

## Components
1. **Dataset**: A collection of movies with attributes such as:
   - Title
   - Overview (description)
   - Genre
   - IMDB Rating
2. **Embedding Model**:
   - Pre-trained SentenceTransformer (`all-MiniLM-L6-v2`) is used to convert textual movie descriptions into vector representations.
3. **Vector Database**:
   - **Pinecone** is used to store and retrieve embeddings efficiently.
   - Movies are upserted into the database with their embeddings and metadata.
4. **Recommendation Engine**:
   - A natural language query (e.g., "show me a murder mystery") is converted into an embedding.
   - The system queries the database for similar movies and returns recommendations.

## Results
Example Query: `"show me a murder mystery"`

![image](https://github.com/user-attachments/assets/f5f17d17-c749-49d8-8423-96c331670d02)


![image](https://github.com/user-attachments/assets/f757a781-8074-4613-aeaa-842cc172e2c3)



## Usage
1. **Environment Setup**:
   - Install required Python libraries:
     ```bash
     pip install sentence-transformers pinecone-client pandas
     ```
2. **Run Notebook**:
   - Execute the Jupyter Notebook step-by-step to prepare data, generate embeddings, and query recommendations.

## Future Improvements
- Expand the dataset with more diverse movie attributes.
- Enhance the embedding model with fine-tuning on movie-related data.
- Incorporate user feedback to refine recommendations.

## Author
Developed by Indrajit.
