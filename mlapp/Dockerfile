# Use the official Python image from the Docker Hub
FROM python:3.7-slim-buster

# Set the working directory inside the container
WORKDIR /app

# Copy the local code to the container's working directory
COPY . /app

# Install the Python dependencies
RUN pip install --no-cache-dir --upgrade -r requirements.txt

# Set the PYTHONPATH to include the src directory
ENV PYTHONPATH "${PYTHONPATH}:/app/src"

# Expose the port on which uvicorn will run
EXPOSE 8000

# Execute the uvicorn server
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000"]
