# backend/Dockerfile
FROM python:3.9-slim

# Environment variables to prevent .pyc files and enable unbuffered output
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set working directory
WORKDIR /app

# Copy and install dependencies
COPY requirements.txt /app/
RUN pip install --upgrade pip && pip install -r requirements.txt

# Copy the Django project code
COPY . /app/

# Expose the port that Django will run on
EXPOSE 8000

# Run Django’s development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
