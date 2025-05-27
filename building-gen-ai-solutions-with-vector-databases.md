# Building Generative AI solutions with Vector Databases
- Vector Databases are designed to store and manage vector data, which represents information in a numerical format that machines can understand.
- Serves as long-term memory that allows AI models to recall relevant information without being re-trained.
- Use cases:
  - Search and recommender systems
  - Computer vision (used to detect audio/videos, used for deep researchs & trainings)
  - Generative AI: allow applications to generate outputs that are relevant to the users and provided contexts.
- Outline:
  - [Vector Search](#vector-search)
  - [Vector Databases](#vector-databases)

## Vector Search
### Vector Distance
- Data (texts, images, videos) can be represented as a vector or list of floating point numbers
- Vecor search is about finding vectors in your dataset taht is closet to a query vector
- Two most common ways to calculate the distances between two vectors: Euclidean distance and cosine distance.
  - Euclidean
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

Example: [Embedding Functions](EmbeddingFunctions.ipynb)

## Vector Databases
### Vector Search Tools
- Vector Index libraries: focus on fast vector search (FAISS, Annoy). Miss data management
- Traditional DBs (Pgvector, Elastic): not scalable and optimized
- Vector Dabases: unstrcutre data management (text, audios, videos), more complete offerings.

### Data Management
- Support vector querying and indexing
  - Querying needs:
      - Filter support to limit results to particular documents. 
      - Post-processing support so we can combine the results with other recallers
  - Indexing needs:
      - Updates: we need to be able to update the database, whereas updating existing entries or adding new ones without indexing the whole thing
      - Versioning: important for AI, for comparison and roll back
- We also need cache and object storage

Example: [Vector Databases Basics](VectorDatabaseBasics.ipynb)

### Advanced Vector Operations
**KNN** is too slow at scale.
**ANN - Approximate Nearest Neighbors**: Trade speed for accuracy. The idea is to reduce the search space
- IVF - Inverted File: index divides the search space into patritions. We only search the patritions closest to the query (1-5% of all the vectors)
- HNSW - Hierarchical Navigable Small Worlds: create multiples layers of graphs where each node is a vector and the edges are the distances between the vectors. We organize the graphs to minimize the number of hops to get to the searched vectors.
**Compressing vectors using Quantization**
- Split the vector(1024x32-bit) into 8 subvectors (128x32-bit)
- Use k-means to create 8-bit clusters that represent the subvectors.
- Since we use the centroid, we may introduce some errors.

Example: [Simple Recommender](SimpleRecommender.ipynb) , [Multimodal Search](MultimodalSearch.ipynb)

