# 💼 Employee Salary Prediction

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python) ![Streamlit](https://img.shields.io/badge/Streamlit-1.35-red?logo=streamlit) ![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4-orange?logo=scikit-learn) ![License](https://img.shields.io/badge/License-MIT-green)

A machine learning-based web application that predicts whether an employee's income is **above or below $50K per year**, based on personal and professional features such as age, education, job role, and experience.

Built as part of an internship project under the guidance of the **Edunet Foundation**. Supports real-time manual input and batch CSV-based predictions through an interactive UI powered by Streamlit.

---

## 🔍 Key Features

- ✔️ Predicts whether an employee's income is **above or below $50K per year**
- ⚙️ **Real-time prediction** via input sliders and dropdowns
- 📂 **Batch prediction** by uploading a `.csv` file (up to 200 MB)
- 👁️ Displays **live preview** of uploaded data
- 🌐 **Deployable** locally or publicly using `pyngrok`/`ngrok`
- 🎛️ Built using **Streamlit** for UI and **scikit-learn** for ML modeling

---

## 🛠️ Technology Stack

- **Programming Language**: Python 3.9+
- **Libraries**:
  - `pandas`, `numpy`, `scikit-learn`
  - `LabelEncoder`, `OneHotEncoder` (feature transformation)
  - `joblib` (model serialisation)
- **Frontend**: Streamlit
- **Web Tunneling**: pyngrok / ngrok (for public deployment)

---

## ⚡ Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/M4ban/Employee-Salary-Prediction.git
cd Employee-Salary-Prediction

# 2. Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt

# 4. Train the model (run all cells in the notebook)
jupyter notebook final_project.ipynb

# 5. Launch the web app
streamlit run streamlit_app.py
```

The app will be available at `http://localhost:8501`.

For detailed setup instructions (virtual environments, ngrok, cloud deployment) see [SETUP.md](SETUP.md).

---

## 🖥️ Demo

| Real-time Prediction | Batch CSV Upload |
|---|---|
| Fill in employee details using sliders and dropdowns and click **Predict** to get an instant result. | Upload a `.csv` file with multiple employee records to receive bulk predictions. |

> 📌 A live demo can be deployed for free on [Streamlit Community Cloud](https://share.streamlit.io).

---

## 📁 Project Structure

```
Employee-Salary-Prediction/
├── final_project.ipynb   # Data exploration, model training & evaluation
├── streamlit_app.py      # Streamlit web application
├── adult.csv             # UCI Adult Census Income dataset
├── requirements.txt      # Python dependencies
├── .gitignore            # Files and folders excluded from version control
├── .editorconfig         # Editor settings for consistent formatting
├── SETUP.md              # Detailed setup & deployment guide
├── LICENSE.md            # MIT License
└── README.md             # Project documentation
```

---

## 📁 Dataset

The application uses the **Adult Census Income Dataset** from the **UCI Machine Learning Repository**.

- 📄 [UCI Adult Dataset](https://archive.ics.uci.edu/ml/datasets/adult)

---

## 🔧 Troubleshooting

| Problem | Solution |
|---|---|
| `ModuleNotFoundError` | Activate the virtual environment and run `pip install -r requirements.txt` |
| `streamlit: command not found` | Run `pip install streamlit` or verify your PATH |
| Model file not found | Run all cells in `final_project.ipynb` first to generate the model artifact |
| Port 8501 already in use | Use `streamlit run streamlit_app.py --server.port 8502` |

---

## 📚 References

- Internship mentorship by **Edunet Foundation**
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [pyngrok Documentation](https://pyngrok.readthedocs.io/)

---

## 🚀 Future Scope

- Integration of a **Flask backend**
- **Database storage** of predictions and user inputs
- User authentication and history tracking for uploaded files

---

## 📄 License

This project is licensed under the [MIT License](LICENSE.md).

---

> ✅ Developed during the AICTE–Edunet Internship with guidance and support from mentors to simulate real-world machine learning deployment and application building experience.
