## Embeddings Basics
- Vector Represenations of items
    - Text
    - Image
    - Video
    - Audio
    - Graph
    - Shared multi-modal 
- Token/Word embeddings (vs) Contextual word embeddings
    - Token/Word embedding models: 
        - A word gets single embedding. E.g. 'bat'. But it could be an animal or sport equipment.
        - Glove, Word2Vec, etc.
    - Contextual word embeddings: 
        - A word gets different embedding based on the sentence/context.
        - Transformer model (BERT, etc.)

## Applications
- LLMs/VLMs/ML models
    - Input tokens are converted to embeddings and given to the LLM/VLM/ML models
- Retrieval
    - Sentence embeddings are used to find relevant data
    - Some applications:
        - Semantic Search
        - Recommendations
        - RAG (LLM/VLM with augmented data)

## Why embedding models in Retrieval?
- Cross-encoder architectures
    - Inputs: Query, Item. Output: Relevance score
    - Accurate but slow. Cannot pre-compute.
- Sentence embedding models
    - Faster. Can pre-compute embeddings for all Items.

## How to build sentence embedding models?
- Sentence embeddings approaches
    - Contextual word embeddings are not accurate enough
        - Average BERT token embeddings
    - SBERT, Sentence-T5, COLBERT, DPR, etc
        - More accurate
- Build Sentence embedding models:
    - Dual encoder + Contrastive learning
    - Bring relevant items closer together
    - Defintion of relevant items depends on application. They could be:
        - Question, Answer pairs
        - Similar items

## How to use sentence embeddings in RAG
- Steps:
    - Chunk the sentence & calcuate embeddings
    - Index them in Vector database
    - Use ANN (Approximate nearest neighbor) algorithms for similarity search/retrieval
        - HNSW, FAISS, Annoy, etc.
- Some frameworks that support Embeddings + RAG
    - Weaviate, Vectara, etc.

## References
1. https://www.deeplearning.ai/short-courses/embedding-models-from-architecture-to-implementation/
    
