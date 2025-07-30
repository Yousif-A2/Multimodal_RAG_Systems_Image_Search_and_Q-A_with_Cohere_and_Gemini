# Multimodal RAG System for Image Search and Q&A

This project demonstrates a multimodal Retrieval-Augmented Generation (RAG) system that allows users to search for images using natural language queries and ask questions about the retrieved images. The system leverages the power of Cohere's multilingual text embeddings and Google's Gemini model for multimodal understanding.

## Features

- **Image Search:** Find relevant images from a collection based on a textual description.
- **Question Answering:** Ask questions about the content of the retrieved images.
- **Multilingual Support:** The system can understand queries in multiple languages (e.g., Arabic).

## How it Works

1. **Image Indexing:**
   - A collection of images is processed.
   - For each image, a base64 representation is generated.
   - Cohere's `embed-v4.0` model is used to create a vector embedding of each image.
   - These embeddings are stored in a searchable index.

2. **Image Search:**
   - A user provides a textual query.
   - The query is embedded using the same Cohere model.
   - The system performs a cosine similarity search between the query embedding and the image embeddings in the index.
   - The most similar image is retrieved.

3. **Question Answering:**
   - The user asks a question about the retrieved image.
   - The question and the image are passed to the Gemini model.
   - Gemini generates an answer based on the visual information in the image.

## Technologies Used

- **Cohere:** For generating high-quality multilingual text and image embeddings.
- **Google Gemini:** For multimodal understanding and question answering.
- **Python:** The primary programming language.
- **Pillow (PIL):** For image manipulation.
- **NumPy:** For numerical operations.
- **Google Colab:** As the development environment.
