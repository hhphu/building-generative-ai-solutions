# Building Generative AI solutions with Vector Databases
- Vector Databases are designed to store and manage vector data, which represents information in a numerical format that machines can understand.
- Serves as long-term memory that allows AI models to recall relevant information without being re-trained.
- Use cases:
  - Search and recommender systems
  - Computer vision (used to detect audio/videos, used for deep researchs & trainings)
  - Generative AI: allow applications to generate outputs that are relevant to the users and provided contexts.
- Outline:
  - [Vector Search](#vector-search)
      - [Vector distance](#vector-distance)
      - [Embedding functions](#embeddings)
  - Basic operations of vector databases
      - Storing and managing data
      - Querying vector databases
  - Indexing
      - KNN (K nearest neighbors) vs ANN
      - ANN techniques

## Vector Search
### Vector Distance
- Data (texts, images, videos) can be represented as a vector or list of floating point numbers
- Vecor search is about finding vectors in your dataset taht is closet to a query vector
- Two most common ways to calculate the distances between two vectors: Euclidean distance and cosine distance.
- K-nearest neighbors: algorithm used to retrieve closest vectors to a query vectror based on the chosen distance metric.
- Example: [Basic Vector Search](BasicVectorSearch.ipynb)

### Embeddings
Embeddings are numerical representations of data.
Use cases:
- Search engines/ recommenders
- Classifications
- Clustering/ deduplication
- Active learning
- Anomaly detection

### BERT: Bi-directional Encoder Represntation from Transformers

![image](https://github.com/user-attachments/assets/00c19f8f-2a99-4104-a6e1-4018abbe7bdf)

- Raw: Receive raw input
- Tokenize: split the inputs and tokenize them
- Embed: generate embedding for each token using the Embedding lookup table
- Extract: Take the average of each token embedding
- Sentence embedding

Example: [Embedding Functions](EmbeddingFunctions.ipybn)
