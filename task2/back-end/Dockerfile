# Use latest Ubuntu
FROM ubuntu:latest

# Update and upgrade
RUN apt-get update && apt-get upgrade -y

# Install python3 and pip3
RUN apt-get install -y python3 python3-pip

# Fix EXTERNALLY-MANAGED error if needed
RUN rm -f /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install flask using pip3
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app
COPY ./api.py /app/api.py

# Expose port 5252
EXPOSE 5252

# Default command to start Flask
CMD ["python3", "api.py"]
