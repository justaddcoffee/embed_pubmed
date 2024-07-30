
# PubMed Sentence Embeddings with Parquet and VenomX Metadata

This Jupyter notebook processes abstracts from about 6000 PubMed articles of particular
interest, generates sentence embeddings using the `all-MiniLM-L6-v2` model from 
Sentence Transformers, and saves  the embeddings in Parquet format. Additionally, 
it generates metadata in VenomX format and uploads the embeddings, metadata, and 
notebook itself to Hugging Face.

## Overview

- **Download PubMed Articles**: Fetch abstracts from PubMed articles based on a list of PMIDs.
- **Generate Sentence Embeddings**: Tokenize abstracts into sentences and generate embeddings for each sentence using `all-MiniLM-L6-v2`.
- **Save Embeddings**: Store the embeddings in Parquet format for efficient storage and retrieval.
- **Generate Metadata**: Create metadata in VenomX format to describe the dataset and model used.
- **Upload to Hugging Face**: Upload the embeddings, metadata, and notebook to a Hugging Face dataset repository.

## Prerequisites

- Python 3.x
- Required Python packages:
  - pandas
  - pyarrow
  - tqdm
  - nltk
  - sentence-transformers
  - huggingface_hub
  - pyyaml

## Usage

1**Clone the repository:**

```bash
git clone https://github.com/justaddcoffee/embed_pubmed.git
```

2**Run the notebook:**

Open the notebook and run each cell sequentially. The notebook performs the following tasks:

- Imports the necessary libraries.
- Reads the PMIDs from the `pmids.txt` file.
- Fetches abstracts from PubMed articles.
- Tokenizes abstracts into sentences and generates embeddings.
- Saves the embeddings in Parquet format.
- Generates metadata in VenomX format.
- Uploads the embeddings, metadata, and notebook to Hugging Face.

## License

This project is licensed under the BSD 3-Clause License.
