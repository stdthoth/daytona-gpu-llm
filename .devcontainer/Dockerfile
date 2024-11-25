# Use an official Python image as a base
FROM python:3.9-slim

# Install system dependencies
RUN apt-get update && apt-get install -y \
    git \
    && rm -rf /var/lib/apt/lists/*

# Set working directory in the container
WORKDIR /workspace

# Install Python dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application files into the container
COPY . .

# Set environment variable for interactive mode
ENV PYTHONUNBUFFERED=1

# Set the default command (you can override this in devcontainer.json)
CMD ["python", "run_model.py"]
