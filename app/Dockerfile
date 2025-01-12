# Dockerfile
FROM python:3.11-alpine

# Set working directory
WORKDIR /code

# Set environment variables
ENV FLASK_APP=app.py
ENV FLASK_RUN_HOST=0.0.0.0

# Install necessary packages
RUN apk add --no-cache gcc musl-dev linux-headers

# Copy requirements and install dependencies
COPY requirements.txt /code/
RUN pip install -r requirements.txt

# Copy application code
COPY app.py /code/

# Define startup command
CMD ["flask", "run"]
