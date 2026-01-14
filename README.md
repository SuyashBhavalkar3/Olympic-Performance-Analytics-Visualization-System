# olympics-data-analysis-web-app
 A Streamlit web application for interactive analysis and visualization of the Olympic athletes dataset.

 Live demo:
 https://olympic-performance-analytics.onrender.com/

 Dataset Link: https://www.kaggle.com/heesoo37/120-years-of-olympic-history-athletes-and-results

 Project structure
 - `app.py` — Streamlit application entrypoint (loads `athlete_events.csv`).
 - `preprocessor.py` — data cleaning and preparation utilities.
 - `helper.py` — helper functions used by the app.
 - `athlete_events.csv` — primary dataset (kept in repository root).
 - `noc_regions.csv` — nation/region lookup table.
 - `requirements.txt` — Python dependencies (includes `streamlit`).
 - `Dockerfile` — container image to run the Streamlit app.
 - `Procfile` & `setup.sh` — deployment helpers (used for Render/Heroku-like hosts).

 Quickstart (local)

 1. Create a virtual environment and activate it.

 ```bash
 python -m venv .venv
 source .venv/bin/activate   # On Windows use: .venv\\Scripts\\activate
 ```

 2. Install dependencies and run the app.

 ```bash
 pip install -r requirements.txt
 streamlit run app.py
 ```

 Docker

 Build and run the provided `Dockerfile`:

 ```bash
 docker build -t olympics-app .
 docker run -p 8501:8501 olympics-app
 ```

 Notes
 - The app expects `athlete_events.csv` to be present in the repository root. Do not remove or rename this file unless you update `app.py` accordingly.
 - The dataset and live demo link above are preserved as-is.

 Contributing
 - Open issues or pull requests for improvements, bugfixes, or documentation updates.

 License
 - See repository root for license information (if present).