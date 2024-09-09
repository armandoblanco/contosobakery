# Use a base Python image
FROM python:3.8

# Copy application files to the container
COPY . /app

# Set the working directory
WORKDIR /app

# Install dependencies
RUN pip install paho-mqtt
RUN pip install influxdb-client

# Set environment variables
ENV MQTT_BROKER=""
ENV MQTT_PORT=1883
ENV MQTT_TOPIC1="topic/productionline"
ENV MQTT_TOPIC2="topic/fryer"
ENV INFLUX_URL=""
ENV INFLUX_TOKEN=""
ENV INFLUX_ORG=""
ENV INFLUX_BUCKET=""

# Command to run the application
CMD ["python", "mqtt-listener.py"]