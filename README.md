# LLM-web-app
LLM-powered web app that allows user to ask questions about uploaded data

## First Time Setup

```
1. Create .env
SECRET_KEY=123
SQLALCHEMY_DATABASE_URI=sqlite:///sqlite.db
UPLOAD_URL=https://prod-upload-langchain.fly.dev

OPENAI_API_KEY=

REDIS_URI=

PINECONE_API_KEY=
PINECONE_ENV_NAME=
PINECONE_INDEX_NAME=

LANGFUSE_PUBLIC_KEY=
LANGFUSE_SECRET_KEY=

2. Install dependencies
pip install -r requirements.txt

# Initialize the database
flask --app app.web init-db
```

## Running the app

There are three separate processes that need to be running for the app to work: the server, the worker, and Redis.

If you stop any of these processes, you will need to start them back up!

Commands to start each are listed below. If you need to stop them, select the terminal window the process is running in and press Control-C

### To run the Python server

```
inv dev
```

### To run the worker

```
inv devworker
```

### To run Redis

```
redis-server
```

### To reset the database

```
flask --app app.web init-db
```


## Running Upload Server Locally

```
cd local-do-files
```

Install dependencies with `pip install -r requirements.txt`

Start the server with `python app.py`

In the pdf project, find the .env file and change the UPLOAD_URL line to the following: UPLOAD_URL=http://localhost:8050

Restart the PDF project


delete:
conda activate pdf
(pdf) root@WDEC044734:~/projects/LLM-web-app# 