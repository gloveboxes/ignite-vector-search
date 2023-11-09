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
python -m venv .venv
```

Linux/macOS

```bash
python3 -m venv .venv
```

## Activate the virtual environment

Windows

```pwsh
.venv\Scripts\activate
```

Linux/macOS

```bash
source .venv/bin/activate
```

## Install the dependencies

```bash
pip install -r requirements.txt
```

## Create an Azure OpenAI Service

Create an Azure OpenAI service and get the API key and endpoint.

1. Sign in with your Azure subscription in the Azure portal.
2. Select Create a resource and search for the `OpenAI`.
3. When you locate the service, select `Create`.
4. On the Create Azure OpenAI page, provide the following information for the fields on the Basics tab: Subscription, Resource group, Region, Name, and Pricing Tier.
5. Select `Next`, then configure the network security settings for your resource. Use the default settings.
6. Select `Next`.
7. Select `Create` to create your resource.

### Create an Embedding Model resource

1. Sign in with your Azure subscription in the Azure portal.
1. Select the Azure OpenAI Service resource you created.
1. Select `Model deployments` from the left-hand menu.
1. Select `Manage Deployment`.
1. Select `+` to create a new deployment.
1. Select `text-embeddings-ada-002` from the `Model` dropdown.
1. Select the default model version.
1. Name the deployment `text-embeddings-ada-002`.
1. Select `Create`.

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
