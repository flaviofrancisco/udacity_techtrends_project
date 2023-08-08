# Use Python base image version 3.8
FROM python:3.8

# Set the working directory inside the container
WORKDIR /app

# Expose the application port 3111
EXPOSE 3111

ADD ./techtrends .

# Install packages defined in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Initialize the database with pre-defined posts
RUN python init_db.py

# Set the command to execute the application at container start
CMD ["python", "app.py"]
