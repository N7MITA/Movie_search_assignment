# Movie Semantic Search Assignment  

This repository contains my solution for Semantic Search on Movie Plots.

## Project Overview

This project builds a semantic search engine for movie plots using SentenceTransformers (all-MiniLM-L6-v2). It transforms plot descriptions into embeddings and leverages cosine similarity to retrieve movies that are most relevant to a user’s query.

## Features  

- **Semantic Search**: Leverages SentenceTransformers to capture the meaning behind user queries.  
- **Cosine Similarity**: Computes similarity scores (0 to 1) to rank movies by relevance.  
- **Flexible Results**: Allows customization of the number of results using the `top_n` parameter.  
- **Automatic Embeddings**: Generates embeddings for all movie plots during initialization for efficient search.



## Setup

### 1. Clone the repository:
```bash
git clone https://github.com/N7MITA/movie-search-assignment.git
cd movie-search-assignment/assignment_1
```

### 2. Create and activate a virtual environment
```bash
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate   # macOS/Linux
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the notebook
```bash
jupyter notebook movie_search_results.ipynb
```

## Testing

Run the unit tests to verify everything works correctly
```bash
python -m unittest tests/test_movie_search.py -v
```

### Expected output: All 4 tests should pass:

- test_search_movies_output_format
  
- test_search_movies_relevance
  
- test_search_movies_similarity_range
  
- test_search_movies_top_n

## Usage

### Example Query
```bash
from movie_search import search_movies
results = search_movies("spy thriller in Paris", top_n=5)
print(results)

Output :
(venv) PS C:\Users\sriva\Desktop\movie-search-assignment\Assignment-1> python movie_search.py
Loaded 3 movies and created embeddings with shape: (3, 384)

Testing search with query: 'spy thriller in Paris'

Top 3 results:
              title                                               plot  similarity
0         Spy Movie  A spy navigates intrigue in Paris to stop a te...    0.769684
1  Romance in Paris  A couple falls in love in Paris under romantic...    0.388029
2      Action Flick  A high-octane chase through New York with expl...    0.256777
```

## Jupyter Notebook

Open movie_search_solution.ipynb and run the cells sequentially to:

1.Import libraries

2.Load the dataset

3.Create embeddings

4.Implement and test the search function


## Files Structure
```bash
assignment_1/
├── movie_search.py              # Main implementation
├── movie_search_solution.ipynb  # Jupyter notebook version
├── movies.csv                   # Sample movie dataset
├── requirements.txt             # Python dependencies
├── tests/
│   └── test_movie_search.py    # Unit tests
└── README.md                    # This file
```



## License
This project is part of the AI Systems Development assignment at IIIT Naya Raipur.
