# Advertiser Data Upload & Validation System

## Project Overview

The Advertiser Data Upload & Validation System is a Flask-based backend application developed using Python.
The system allows users to upload advertiser campaign data through Excel files, validate the uploaded data, calculate CTR (Click Through Rate), and store the processed data in a SQLite database.

This project demonstrates:

* REST API Development
* Data Validation
* Database Handling
* Automation Workflows
* Backend Development
* Data Processing Pipelines

---

# Features

* Upload advertiser data using Excel files
* Validate uploaded dataset columns
* Calculate CTR automatically
* Store advertiser data in SQLite database
* Fetch stored data using APIs
* Error handling and validation
* REST API implementation using Flask

---

# Technologies Used

* Python
* Flask
* Pandas
* SQLite
* OpenPyXL
* REST APIs

---

# Project Structure

```bash
Advertiser_Project/
│
├── app.py
├── advertiser_data.xlsx
├── advertiser_data.db
├── uploads/
└── README.md
```

---

# Installation

## Step 1: Clone or Download Project

Download the project folder and open it in VS Code or any Python IDE.

---

## Step 2: Install Required Packages

Run the following command in terminal:

```bash
pip install flask pandas openpyxl
```

---

# Running the Project

Run the following command:

```bash
python app.py
```

Server will start on:

```bash
http://127.0.0.1:5000
```

---

# API Endpoints

## 1. Home API

### Endpoint

```bash
GET /
```

### URL

```bash
http://127.0.0.1:5000/
```

### Response

```json
Advertiser Data Upload API Running Successfully
```

---

## 2. Upload Excel File API

### Endpoint

```bash
POST /upload
```

### URL

```bash
http://127.0.0.1:5000/upload
```

### Request Type

* form-data
* Key = file
* Upload Excel File

### Sample Response

```json
{
  "status": "SUCCESS",
  "message": "Data uploaded successfully",
  "records_uploaded": 10
}
```

---

## 3. Fetch Advertiser Data API

### Endpoint

```bash
GET /advertisers
```

### URL

```bash
http://127.0.0.1:5000/advertisers
```

### Sample Response

```json
[
  {
    "advertiser_name": "Amazon",
    "campaign_name": "Summer Sale",
    "impressions": 10000,
    "clicks": 500,
    "ctr": 5.0
  }
]
```

---

# Database Schema

| Column Name     | Data Type |
| --------------- | --------- |
| id              | INTEGER   |
| advertiser_name | TEXT      |
| campaign_name   | TEXT      |
| impressions     | INTEGER   |
| clicks          | INTEGER   |
| country         | TEXT      |
| platform        | TEXT      |
| budget          | INTEGER   |
| ctr             | REAL      |
| upload_time     | TEXT      |

---

# CTR Formula

CTR (Click Through Rate) is calculated using:

```text
CTR = (Clicks / Impressions) * 100
```

---

# Sample Dataset Columns

The uploaded Excel file must contain:

* advertiser_name
* campaign_name
* impressions
* clicks
* country
* platform
* budget

---

# Future Improvements

* JWT Authentication
* MySQL Integration
* Cloud Deployment
* API Security
* Docker Support
* Automated Reporting Dashboard
* CI/CD Pipeline Integration

---

# Skills Demonstrated

* Backend Development
* REST APIs
* SQL Database Handling
* Data Validation
* Automation Scripting
* Flask Framework
* Error Handling
* Data Processing Pipelines

---

# Author

Sejal Jadhav

LinkedIn: linkedin.com/in/sejal-jadhav24

GitHub: github.com/sejalj247
