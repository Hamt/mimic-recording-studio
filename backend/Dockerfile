FROM python:3.6-alpine3.6
# Set the working directory
WORKDIR /src

# Copy requirements file
COPY requirements.txt .

# Update apk repositories
RUN apk update

# Install necessary packages
RUN apk add --no-cache ffmpeg make automake gcc g++ subversion python3-dev sqlite-dev

# Upgrade pip
RUN pip install --upgrade pip

# Install Python dependencies
RUN pip install -r requirements.txt

# Add command to run your application
CMD ["sh", "start_prod.sh"]

