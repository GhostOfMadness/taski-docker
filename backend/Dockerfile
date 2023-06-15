# Base image
FROM python:3.9-slim

# Set working directory
WORKDIR /app

# Install gunicorn
RUN pip install gunicorn==20.1.0

# Copy requirement file
COPY requirements.txt .

# Install project dependencies
RUN pip install -r requirements.txt --no-cache-dir

# Copy project files
COPY . .

# Start Gunicorn WSGI server
CMD ["gunicorn", "--bind", "0.0.0.0:8000", "backend.wsgi"]

