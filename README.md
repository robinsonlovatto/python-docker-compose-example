# Python Docker Example
A simple project that creates a Streamlit page to learn Docker Compose.

## Starting the project from scratch
```bash
pyenv local 3.12.1   
poetry init    
poetry env use 3.12.1     
poetry shell     
poetry add streamlit    
poetry add psycopg2
```

## Cloning the project
```bash
git clone https://github.com/robinsonlovatto/python-docker-compose-example.git
cd python-docker-compose-example
poetry shell
poetry install
```

## Building Docker image and running it
```bash
# to build only the streamlit app image
docker build -t my-python-image .
# to run only the streamlit app container
docker run -d -p 8501:8501 --name my-python-container my-python-image
# to run the entire solution (postgresql + pgadmin + streamlit app)
docker compose up
```






