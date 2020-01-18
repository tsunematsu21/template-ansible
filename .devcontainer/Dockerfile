FROM python:3.8.1-buster

ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update \
 && apt-get install -y --no-install-recommends \
    apt-utils \
    dialog \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

# Install requirements packages by pip
COPY requirements.txt .
RUN pip install --user -r requirements.txt

ENV PATH=/root/.local/bin:$PATH
