# Hybrid Image Search with Pinecone

This project demonstrates how to build a hybrid image search system using Pinecone, combining both sparse (text-based) and dense (image-based) vectors. It uses a fashion product dataset and integrates a retrieval model with images and metadata. The search results are optimized using both text-based keywords and image similarity.

## Prerequisites

Make sure you have the following installed:

- Python 3.7+
- Pip (Python package installer)

You will also need an API key for Pinecone and access to the Open Fashion Product Images dataset.

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/integrader/image-search.git
    ```

2. Navigate to the project directory:

    ```bash
    cd image-search
    ```



## Setup Pinecone

1. Create an account on Pinecone and get your API key from [Pinecone's website](https://www.pinecone.io/).
2. Set your API key as an environment variable:

    ```bash
    export PINECONE_API_KEY="your-pinecone-api-key"
    ```

3. Optionally, you can set the cloud provider and region as environment variables:

    ```bash
    export PINECONE_CLOUD="aws"
    export PINECONE_REGION="us-east-1"
    ```

## Dataset

This project uses the Open Fashion Product Images dataset, which can be loaded directly from Hugging Face.

```python
from datasets import load_dataset

fashion = load_dataset("ashraq/fashion-product-images-small", split="train")
