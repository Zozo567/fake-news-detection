from gcr.io/datamechanics/spark:platform-3.1-dm14

ENV PYSPARK_MAJOR_PYTHON_VERSION=3
WORKDIR /opt/application/

COPY requirements.txt .

RUN pip3 install --upgrade pip  --user
RUN pip3 install -r requirements.txt

COPY . .

EXPOSE 4040

COPY main.py .
COPY stream.py .

# waiting for spark warming up
# CMD ["sleep", "30"]

# CMD ["python", "main.py"]


# stream % docker build -t streamingservicev12 -f Dockerfile.test .