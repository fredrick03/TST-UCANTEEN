# Use the official Python image from the Docker Hub
FROM python:3

# Set the working directory inside the container
ADD main.py .

# Copy the current directory contents into the container at /app
COPY . /TST-UCANTEEN
WORKDIR /TST-UCANTEEN

# Install any necessary dependencies
RUN pip install fastapi uvicorn SQLalchemy pydantic[email] pydantic-settings pymysql python-jose[cryptography] PyJWT passlib shapely haversine python-multipart bcrypt

# Command to run the FastAPI server when the container starts
CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "80"]