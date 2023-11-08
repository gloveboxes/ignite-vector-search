# Vector search with Azure Gognitive Search

## Prerequisites

- Windows, Linux, or macOS
- Tested on [Python 3.11.6](https://www.python.org/downloads/)

## Clone the repository

Open a terminal and clone the repository:

```bash
git clone https://github.com/gloveboxes/ignite-vector-search.git
```

Change to the `ignite-vector-search` directory:

```bash
cd ignite-vector-search
```

## Create a virtual environment

Windows

```pwsh
python3 -m venv .venv
```

Linux/MacOS

```bash
python -m venv .venv
```

## Activate the virtual environment

Windows

```pwsh
.venv\Scripts\activate
```

Linux/MacOS

```bash
source .venv/bin/activate
```

## Install the dependencies

```bash
pip install -r requirements.txt
```

## Create the Azure Cognitive Search service

Follow the notes at [Use the REST API to run vector search queries](https://microsoftlearning.github.io/mslearn-knowledge-mining/Instructions/Labs/10-vector-search-exercise.html)

1. Create the Azure Cognitive Search service
2. Create the index
3. Upload the documents

## Set the environment variables

- `AZURE_OPENAI_API_KEY` - Your OpenAI API key
- `AZURE_OPENAI_ENDPOINT` - Your OpenAI endpoint
- `AZURE_COG_SEARCH_API_KEY` - Your Azure Cognitive Search API key
- `AZURE_COG_SEARCH_ENDPOINT` - Your Azure Cognitive Search endpoint

## Run the examples

There are 3 examples in the `notebooks` folder:

1. Content embedding (notebooks/content_embedding.ipynb)
   Example of how to create the content embedding
1. Query embedding (notebooks/query_embedding.ipynb)
   Example of how to create the query embedding and run a query against Azure Cognitive Search
1. Full solution (notebooks/solution.ipynb)
   End-to-end example how to query Azure Cognitive Search using the content and query embedding
