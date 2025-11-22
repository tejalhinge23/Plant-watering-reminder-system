# Plant-watering-reminder-system
🌱 IoT-Based Plant Watering Reminder System using AWS IoT Core
📌 Project Overview

This project is an IoT-based Plant Watering Reminder System that monitors real-time soil moisture levels using an ESP32 microcontroller and sends water reminders to the user through AWS cloud services. The system helps users ensure that their plants receive timely watering, preventing both overwatering and underwatering.

The device reads moisture values from a soil sensor and securely publishes the data to AWS IoT Core using MQTT. AWS IoT rules trigger a Lambda function, which stores the data in DynamoDB and sends alert notifications through Amazon SNS whenever the moisture level drops below a defined threshold.

🚀 Features

📡 Real-time soil moisture monitoring via ESP32

🔐 Secure MQTT communication using AWS IoT Core certificates

☁️ Serverless backend built with AWS Lambda

📦 Data storage using DynamoDB for historical moisture tracking

🔔 SMS/Email alerts via Amazon SNS when plant needs watering

📊 Easy to extend for dashboards using AWS QuickSight / IoT Analytics

🛠️ System Architecture

ESP32 + Soil Moisture Sensor

Reads moisture level

Publishes data to MQTT topic: plants/{deviceId}/telemetry

AWS IoT Core

Manages device authentication and MQTT messaging

IoT Rule forwards messages to Lambda

AWS Lambda Function

Parses incoming sensor data

Saves it to DynamoDB

Sends reminders through SNS when moisture is low

DynamoDB Table

Stores timestamped moisture readings

Helps track plant watering history

Amazon SNS

Sends plant watering notifications (SMS/Email)

📡 Hardware Requirements

ESP32 development board

Capacitive soil moisture sensor

Jumper wires

Power supply / USB cable

☁️ AWS Services Used

AWS IoT Core

AWS Lambda

Amazon DynamoDB

Amazon SNS

CloudWatch (logging)

📂 Project Workflow

ESP32 measures soil moisture

ESP32 publishes data to AWS IoT Core using MQTT

IoT Rule triggers Lambda function

Lambda stores data in DynamoDB

If moisture < threshold → SNS sends alert

User receives "Plant needs watering" message

🎯 Use Cases

Home gardening

Smart agriculture

Office plant maintenance

Educational IoT projects

✔️ Key Benefits

Reduces plant dehydration risk

Automates monitoring

Serverless and low maintenance

Works anywhere with Wi-Fi

📝 Future Improvements

Add mobile dashboard for live monitoring

Control a water pump (automatic irrigation)

Add battery monitoring

Integrate with AWS Timestream for time-series analytics

Add multiple plant support with unique device IDs
