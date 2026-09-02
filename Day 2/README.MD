# Mini Semantic Search Engine with FAISS

A lightweight, fast semantic search engine built in Python using Meta's **FAISS** (Facebook AI Similarity Search) vector store and Hugging Face's `sentence-transformers`. 

This project demonstrates vector indexing, $L_2$ normalization for cosine similarity search, dense vector generation, and an interactive command-line search loop.

---

##  Features & Assignment Tasks Completed

- **Task 1: Embedding Generation**: Embedded a 10-sentence customer service knowledge base into a $(10, 384)$ vector matrix using `sentence-transformers/all-MiniLM-L6-v2`.
- **Task 2: FAISS Indexing**: Built a `faiss.IndexFlatL2` index with normalized vectors using `faiss.normalize_L2()` to achieve exact Cosine Similarity behavior.
- **Task 3: Semantic Search**: Performed Top-3 similarity searches on multiple test queries, outputting distance scores and matched knowledge-base items.
- **Task 4: Interactive CLI**: Built a continuous terminal input loop supporting real-time search queries until the user types `exit`.

---

##  Repository Structure

```text
faiss-semantic-search/
├── faiss_semantic_search.py   # Complete implementation code
├── requirements.txt            # Dependency list
└── README.md                   # Project documentation
