# Real-Time Twitter Sentiment Pipeline
This project is a real-time data pipeline that captures tweets using the Twitter API, streams them through Apache NiFi and Kafka, analyzes their sentiment with a fine-tuned RoBERTa model, and dynamically visualizes public sentiment using Matplotlib.
In this project i focused capturing real-time opinions from X(Formerly Twitter) about Safaricom (A telecommunication company in Kenya)

## Features
Collects tweets on specific keywords ("Safaricom") in real-time

Streams data using Apache NiFi and Kafka

Uses Hugging Face Transformers (RoBERTa) for sentiment analysis (Positive, Neutral, Negative)

Real-time visualization of sentiment trends

# Technologies Used
Python

Apache NiFi

Apache Kafka

Hugging Face Transformers

Matplotlib

Twitter API v2

# Project Architecture
Twitter API → Collects tweets using tweet_mode=extended

Apache NiFi → Ingests and routes tweets to Kafka

Apache Kafka → Buffers real-time data streams

Python Consumer → Consumes tweets, runs sentiment model

Matplotlib Plot → Dynamically updates sentiment chart



## Sentiment Model
A pretrained cardiffnlp/twitter-roberta-base-sentiment model is used for classifying tweet sentiment.


## Sample Tweet
"Safaricom linking PayPal with Mpesa was the best thing they did this year!"

→ Sentiment: Positive

## Visual output of analysed opinions
The analysis indicated that many people who mentioned Safaricom in their tweets were neutral. The figure below shows the visual output of the opnions which were analysed.

<img width="844" height="455" alt="Sentiment Visual" src="https://github.com/user-attachments/assets/6c9d2316-44ef-4868-ba16-7f92233b8bf0" />
