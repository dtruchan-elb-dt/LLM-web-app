# LLM-web-app
LLM-powered web app that allows user to ask questions about uploaded data

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

2. Initialize the database
`flask --app app.web init-db`
