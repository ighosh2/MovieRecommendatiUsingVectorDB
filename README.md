#Movie Recommendation System Using Vector Database

##Project Overview
This project demonstrates the implementation of a movie recommendation system using vector embeddings and a vector database (Pinecone). The system leverages machine learning models for generating embeddings from movie descriptions and performs similarity searches to recommend movies based on a user's query.

##Features
Data Preparation: Processes and refines a dataset of movies, including their titles, genres, IMDB ratings, and descriptions.
Embedding Generation: Utilizes the pre-trained SentenceTransformer model (all-MiniLM-L6-v2) to encode movie descriptions into numerical vectors.
Vector Database Integration: Stores the embeddings in Pinecone, a cloud-based vector database, along with metadata for each movie.
Querying for Recommendations: Accepts a natural language query from the user and retrieves the top similar movies based on embedding similarity.
Components
Dataset: A collection of movies with attributes such as:
Title
Overview (description)
Genre
IMDB Rating
Embedding Model:
Pre-trained SentenceTransformer (all-MiniLM-L6-v2) is used to convert textual movie descriptions into vector representations.
Vector Database:
Pinecone is used to store and retrieve embeddings efficiently.
Movies are upserted into the database with their embeddings and metadata.
Recommendation Engine:
A natural language query (e.g., "show me a murder mystery") is converted into an embedding.
The system queries the database for similar movies and returns recommendations.
How It Works
Prepare Dataset:
Process the movie dataset and assign unique IDs to each movie.
Encode each movie's description into a 384-dimensional vector using the embedding model.
Upload to Vector Database:
Store embeddings along with metadata in Pinecone.
Metadata includes title, genre, description, and IMDB rating.
Querying for Recommendations:
User inputs a query describing the kind of movies they are interested in.
Query is encoded into an embedding and compared with stored movie embeddings.
Top matching movies are returned as recommendations.
