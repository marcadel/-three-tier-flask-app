# Use an official Python runtime as a parent image
FROM python:3.13.0a1-alpine

# Set the working directory in the container
WORKDIR /app

# Copy the requirements file into the container
COPY requirements.txt requirements.txt

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Run
CMD [ "gunicorn", "wsgi:app", "--bind=0.0.0.0:5000" ]
# CMD ['python']