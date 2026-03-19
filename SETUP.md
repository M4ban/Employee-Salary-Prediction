# Setup Guide – Employee Salary Prediction

This guide walks you through setting up the project from scratch on your local machine.

---

## Prerequisites

- Python 3.9 or higher
- pip (comes with Python)
- Git

---

## 1. Clone the Repository

```bash
git clone https://github.com/M4ban/Employee-Salary-Prediction.git
cd Employee-Salary-Prediction
```

---

## 2. Create a Virtual Environment

**macOS / Linux**
```bash
python3 -m venv venv
source venv/bin/activate
```

**Windows (Command Prompt)**
```cmd
python -m venv venv
venv\Scripts\activate
```

**Windows (PowerShell)**
```powershell
python -m venv venv
venv\Scripts\Activate.ps1
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 4. Run the Jupyter Notebook

The notebook (`final_project.ipynb`) covers data exploration, model training, and evaluation.

```bash
jupyter notebook final_project.ipynb
```

Run all cells in order to train the model and export the serialised model artifact (e.g. `model.pkl`).

---

## 5. Run the Streamlit App

After the model has been trained and saved, launch the interactive web application:

```bash
streamlit run streamlit_app.py
```

Open the URL shown in your terminal (usually `http://localhost:8501`) in a browser.

---

## 6. Public Deployment with ngrok / pyngrok

To share a live demo without a cloud account, use pyngrok (already included in `requirements.txt`).
Add the following snippet to the bottom of `streamlit_app.py` (or run it separately) **after** starting Streamlit:

```python
from pyngrok import ngrok
public_url = ngrok.connect(8501)
print("Public URL:", public_url)
```

---

## 7. Deployment on Streamlit Community Cloud

1. Push your repository to GitHub.
2. Visit [share.streamlit.io](https://share.streamlit.io) and sign in with GitHub.
3. Click **New app**, select your repository, branch, and `streamlit_app.py` as the main file.
4. Click **Deploy** – Streamlit will install `requirements.txt` automatically.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| `ModuleNotFoundError` | Make sure the virtual environment is activated and run `pip install -r requirements.txt` |
| `streamlit: command not found` | Run `pip install streamlit` or check your PATH |
| Model file not found | Run the Jupyter notebook first to generate the model artifact |
| Port 8501 already in use | Run `streamlit run streamlit_app.py --server.port 8502` |
| ngrok auth error | Run `ngrok config add-authtoken <your_token>` (free token from [ngrok.com](https://ngrok.com)) |
