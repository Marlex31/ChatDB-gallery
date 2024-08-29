
# ChatDB
## A Text-to-SQL interface

![Picture of the initial frontend](/demo/frontend.png)

## [Video Demo](https://streamable.com/wqvo69)

## Description

Given an SQL database, ChatDB dynamically generates comprehensive prompts that contain information about your database schema and the meaning of each column.

This information is then used by an LLM to generate SQL to extract the relevant data, and return it in a interactive graphic or text summary.

## Gallery

Query: "Graph a line chart of beer sales in the 2023-24 period."

![Beer sales graph](/demo/beer-sales-graph.png)


Query: "At what hours do most beer sales usually occur?"

![Beer sales by hour](/demo/beer-sales-hours.png)


Query: "Using 2023 beer sales, what do you forecast future sales will look like?"

![Forecasting beer sales](/demo/forecast.png)

## How to run

#### Pre-requisites
A PostgreSQL connection is required.

You can instantiate the inference `llm` class with different services or LLMs which require (see docstring for more):

* OpenAI API key in environment variable `OPENAI_API_KEY` (see docs)

* path to local `.gguf` file

* HuggingFace🤗 model link

### With frontend

#### Dev environment

`fastapi dev main_api.py`

#### Production

`fastapi run main_api.py`

#### Open `http://127.0.0.1:8000/`

### CLI interface

#### `python main.py`
