# 💼 Employee Salary Prediction

This is a machine learning-based web application developed to predict employee salary categories (above or below $50K per year) based on personal and professional features such as age, education, job role, and experience.

The application was built as part of an internship project under the guidance of the **Edunet Foundation**. It supports both real-time input and batch CSV-based predictions through a clean, interactive UI powered by Streamlit.

---

## 🔍 Key Features

- ✔️ Predicts whether an employee’s income is **above or below $50K per year**
- ⚙️ **Real-time prediction** via input sliders and dropdowns
- 📂 **Batch prediction** by uploading a `.csv` file (up to 200MB)
- 👁️ Displays **live preview** of uploaded data
- 🌐 **Deployable** locally or publicly using `pyngrok`/`ngrok`
- 🎛️ Built using **Streamlit** for UI and **scikit-learn** for ML modeling

---

## 🛠️ Technology Stack

- **Programming Language**: Python
- **Libraries**:
  - `pandas`, `numpy`, `scikit-learn`
  - `LabelEncoder`, `OneHotEncoder` (feature transformation)
  - `joblib` (model serialization)
- **Frontend**: Streamlit
- **Web Tunneling**: pyngrok / ngrok (for public deployment)

---

## 📁 Dataset

The application uses the **Adult Census Income Dataset** from the **UCI Machine Learning Repository**, provided in CSV format during the internship.

- 📄 [UCI Adult Dataset](https://archive.ics.uci.edu/ml/datasets/adult)

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

> ✅ Developed during the AICTE–Edunet Internship with guidance and support from mentors to simulate real-world machine learning deployment and application building experience.

---

Let me know if you’d like me to add badges, images, deployment instructions (e.g. for ngrok), or a contributing/license section as well!


## 📁 Project Structure
├── salary_app.ipynb # Jupyter Notebook for data exploration, training, evaluation
├── streamlit_app.py # Streamlit web application to serve the model
├── requirements.txt # Python dependencies
├── README.md # Project documentation
