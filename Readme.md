# Track 2: BigQuery Data Agent 📊🤖

[![Deployed on Render](https://img.shields.io/badge/Deployed_on-Render-46E3B7?logo=render&logoColor=white)](https://track-2-bq-data-agent.onrender.com/)
[![Challenge](https://img.shields.io/badge/Challenge-AccelerateAIwithCloudRun-orange)](#)

This repository contains the Track 2 submission for the **Google Cloud Gen AI Academy Challenge**. It delivers an internal-facing data analyst agent capable of translating natural language queries into insights using Google BigQuery and the Gemini API.

## 🌟 Overview
Built for business users, this agent democratizes data access by allowing team members to ask complex data questions in plain English. The agent processes the request, interacts with BigQuery schemas, and synthesizes the data into readable insights.

## 🚀 Live Demo
**[https://track-2-bq-data-agent.onrender.com/](https://track-2-bq-data-agent.onrender.com/)**

[View Track 2 Demo Screenshot](track-2-demo.pdf)

*(Note: Hosted on a free Render instance. Please allow ~30–50 seconds for the initial load if the server is waking up from sleep mode.)*

## 🚀 Key Architectural Highlights
* **Data Engine:** Integrated with `google-cloud-bigquery` for enterprise data warehousing.
* **AI Engine:** Powered by `gemini-3.6-flash` for high-speed natural language to SQL translation and data summarization.
* **Serverless Deployment:** Fully containerized and hosted on **Render** (originally built for Google Cloud Run).

## 📁 Repository Structure
* `app.py`: Flask web application, BigQuery client initialization, and Gemini orchestration.
* `Dockerfile`: Container configuration optimized for cloud deployment.
* `requirements.txt`: Python package dependencies including GCP libraries.

## ☁️ Deployment Reference
This agent was originally deployed to Cloud Run using the following Google Cloud SDK command (now hosted on Render using the same containerization approach):
```bash
gcloud run deploy bq-data-agent \
  --source . \
  --region us-central1 \
  --set-env-vars GEMINI_API_KEY="AQ.XXXXXXXXXxgA" \
  --allow-unauthenticated
