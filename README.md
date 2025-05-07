# Create virtual env

python -m venv venv

# Create requirement file 
pip3 freeze > requirements.txt

# Build docker image
docker build -t marker-service .

# Run container
docker run -d --name marker-service -p 5000:8501 marker-service