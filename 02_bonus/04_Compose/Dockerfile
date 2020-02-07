FROM python:3.7-alpine

WORKDIR /code

ENV FLASK_APP app.py

ENV FLASK_RUN_HOST 0.0.0.0

RUN apk add --no-cache gcc musl-dev linux-headers

COPY requirements.txt requirements.txt

RUN pip install -r requirements.txt

COPY . .

CMD ["flask", "run"]

# This tells Docker to:

# Build an image starting with the Python 3.7 image.
# Set the working directory to /code.
# Set environment variables used by the flask command.
# Install gcc so Python packages such as MarkupSafe and SQLAlchemy can compile speedups.
# Copy requirements.txt and install the Python dependencies.
# Copy the current directory . in the project to the workdir . in the image.
# Set the default command for the container to flask run
