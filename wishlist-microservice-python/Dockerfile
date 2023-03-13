# Set the base image to Python 3.10 with Alpine
FROM python:3.10-alpine

# Copy the entire project to the container
COPY . .

# Install Flask and Flask-CORS using pip
RUN pip install flask flask_cors

# Expose port 1003 for the application
EXPOSE 1003

# Start the application using the `python` command
CMD ["python", "index.py"]



# FROM python:3
# COPY . .
# RUN pip install flask flask_cors
# EXPOSE 1003
# CMD ["python","index.py"]