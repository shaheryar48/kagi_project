Warmup Task:

Features

Fetch Top Stories:

Retrieves the top 500 story IDs from Hacker News using the Hacker News API.

Story Details:

Fetches story details (title, text, and URL) for each story in parallel using ThreadPoolExecutor to improve performance.

Text Preprocessing:

Cleans and standardizes text by removing special characters, converting to lowercase, and trimming extra spaces.

Semantic Similarity Ranking:

Uses the sentence-transformers library to generate embeddings for the user bio and story content.

Computes cosine similarity between the bio and each story to rank them.

User-Friendly Interface:

Simple HTML form for users to input their bio.

Displays ranked stories with similarity scores and clickable links.

How It Works

User Input:

Users enter their bio through a web form.

Fetch Top Stories:

The app retrieves the top 500 story IDs from Hacker News.

Process Story Details:

Fetches the details for each story (title, text, and URL).

Combines and preprocesses the title and text for ranking.

Compute Similarity:

Encodes the user bio and story content using the paraphrase-MiniLM-L6-v2 model from the sentence-transformers library.

Ranks the stories based on cosine similarity scores.

Display Results:

Returns an HTML page with the ranked stories, their similarity scores, and links to the original stories.
