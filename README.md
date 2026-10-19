# Phishing URL Detector

An ML-based cybersecurity project that analyzes URLs to predict potential phishing threats and explains suspicious URL characteristics through a security risk report.

## Features

- **Machine Learning Prediction:** Classifies submitted URLs using the project's trained model.
- **URL Feature Analysis:** Displays extracted URL characteristics used by the detection pipeline.
- **Security Risk Explanation:** Highlights warning signals such as IP-based hosts, suspicious keywords, URL shorteners, missing HTTPS, multiple subdomains, and unusually long URLs.
- **Interactive Web Interface:** Built with Streamlit for easy URL testing.
- **URL History:** Stores previously checked URLs locally using SQLite.
- **Model Evaluation:** Includes project scripts for running tests and generating evaluation reports.

## Tech Stack

- Python
- Streamlit
- Scikit-learn
- Pandas and NumPy
- SQLite
- URL parsing and feature extraction

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/komal-k25/Phishing-URL-Detector.git
cd Phishing-URL-Detector
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run the application

```bash
python -m streamlit run app.py
```

The application should open in your browser.

## Security Risk Explanation

The application provides additional context about potentially suspicious URL characteristics. These indicators are warnings, not proof that a website is malicious.

A URL without detected warning signals can still be a phishing URL. The risk explanation does not independently verify website ownership, certificate validity, or live threat intelligence.

## Project Structure

```text
Phishing-URL-Detector/
├── app.py
├── run_all.py
├── requirements.txt
├── README.md
├── data/
├── features/
├── model/
├── reports/
├── src/
└── tests/
```

## Limitations

- Predictions depend on the trained model and the features available to it.
- Model performance depends on the quality and representativeness of its training and evaluation data.
- URL-based checks alone cannot guarantee that a website is safe.
- This project is intended for educational and research purposes, not as a replacement for professional security tools.

## Future Improvements

- Integrate trusted threat-intelligence feeds.
- Expand testing with diverse phishing and legitimate URL datasets.
- Improve model evaluation and explainability.
- Add more URL and domain-level security checks.

## Disclaimer

This project is for educational purposes. Always verify suspicious links independently and avoid entering sensitive information on untrusted websites.
