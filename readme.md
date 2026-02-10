# Sensor API (Flask + SQLite)

This is a simple backend REST API inspired by the UCSC OSRE ENTS project.
It stores sensor readings in a SQLite database and provides endpoints to fetch, analyze, and export the data.

## Features
- Add sensor readings
- Fetch readings (optionally filtered by sensor type)
- Get statistics (min/max/avg)
- Export readings as CSV
- Built using Flask + SQLAlchemy + SQLite

## Tech Stack
- Python
- Flask
- SQLite
- SQLAlchemy

---

## Folder Structure

sensor_api/
│── app/
│ │── __init__.py
│ │── config.py
│ │── database.py
│ │
│ │── models/
│ │ │── reading.py
│ │
│ │── routes/
│ │ │── readings.py
│ │ │── stats.py
│ │
│ │── utils/
│ │ │── csv_export.py
│
│── requirements.txt
│── run.py
│── README.md


---

## Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/your-username/ents-sensor-api.git
cd ents-sensor-api

### 2. Create a virtual environment
python -m venv venv
Activate it:

#Windows:
venv\Scripts\activate

#Linux/Mac:
source venv/bin/activate

#3.Install dependencies
pip install -r requirements.txt

#4.Run the server
python run.py

Server will start at:
http://127.0.0.1:5000

Stats endpoint(for min/max/avg)
http://127.0.0.1:5000/api/stats?sensor=temperature

CSV export endpoint (it should download a csv file)
http://127.0.0.1:5000/api/readings/export/csv?sensor=temperature

to see inserted data
http://127.0.0.1:5000/api/readings




