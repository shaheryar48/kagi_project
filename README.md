Warmup Task

1. The app retrieves the top 500 story IDs from Hacker News and fetches their details (title, text, and URL) using the Hacker News API.
2. User input (a bio) is collected and preprocessed by cleaning text and removing special characters.
3. Story content is combined and preprocessed similarly, then encoded into embeddings using the sentence-transformers library.
4. Cosine similarity is computed between the user bio and story embeddings to rank stories by relevance.
5. The ranked stories, along with similarity scores, are displayed as clickable links in a simple HTML interface.


Main Task

1. Fine Tuned Flan-T5 small model using the dataset available at https://huggingface.co/datasets/lapp0/hotpot_query_expansion_synthetic_cleaned. Started seeing results same as given in the task.
2. Converted the model using ctranslate2 library for faster inferencing. In addition to this 8-bit quantization was also done, quantized model is in the optimized_model directory. Reduced the model to 75 mb from 308 mb. This allowed for much faster inferencing within 100 ms.
3. Made an API using flask to view results.
