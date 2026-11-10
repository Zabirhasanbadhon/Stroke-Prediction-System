# 🧠 Stroke Prediction Web App

<p align="center">
  <strong>Predict. Understand. Raise Awareness.</strong>
  <br />
  A machine learning-powered web application that estimates stroke likelihood using health and demographic information.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10%2B-blue?logo=python" />
  <img src="https://img.shields.io/badge/Flask-Web%20Framework-black?logo=flask" />
  <img src="https://img.shields.io/badge/Scikit--learn-Machine%20Learning-F7931E?logo=scikitlearn" />
  <img src="https://img.shields.io/badge/Bootstrap-5-purple?logo=bootstrap" />
  <img src="https://img.shields.io/badge/License-MIT-green" />
</p>

---

## 📌 Overview

**Stroke Prediction Web App** is a modern machine learning application designed to estimate the likelihood of a stroke based on user-provided health and demographic information.

Built with **Python, Flask, Scikit-learn, and Bootstrap 5**, the application provides a simple and responsive interface where users can enter health details and receive an instant prediction.

The model considers important factors such as:

- Age
- Average glucose level
- Body Mass Index (BMI)
- Hypertension
- Heart disease
- Smoking status
- Lifestyle and demographic information

The application displays the prediction as **Likely** or **Not Likely**, with a clean, color-coded result interface.

## ✨ Features

| Feature | Description |
|---|---|
| 🧠 Machine Learning | Predicts stroke likelihood using a trained ML model |
| 🎨 Modern UI | Glassmorphism cards, gradients, and smooth animations |
| 📱 Responsive Design | Compatible with desktop, tablet, and mobile |
| ⚡ Instant Prediction | Real-time results using Flask |
| 📝 Organized Form | Separate personal information and health sections |
| 🎯 Result Dashboard | Color-coded prediction with icons and guidance |
| 🔒 Privacy Focused | No application-level storage of submitted predictions |
| 🛠️ Preprocessing Pipeline | Uses a saved preprocessing system with the trained classifier |

---

## 🛠️ Tech Stack

| Category | Technology |
|---|---|
| Programming Language | Python |
| Backend | Flask |
| Machine Learning | Scikit-learn |
| Data Processing | Pandas |
| Model Serialization | Joblib |
| Frontend | HTML5, CSS3 |
| UI Framework | Bootstrap 5 |
| Icons | Font Awesome |
| Typography | Google Fonts – Inter |

---

## 📂 Project Structure

```text
stroke-prediction/
│
├── app.py                    # Flask application
├── model.joblib              # Trained ML model and preprocessor
├── requirements.txt          # Python dependencies
├── README.md                 # Project documentation
├── LICENSE                   # MIT License
│
├── templates/
│   ├── index.html            # Input form page
│   └── result.html           # Prediction result page
│
└── docs/
    ├── index.png             # Input form screenshot
    ├── result-likely.png     # Likely prediction screenshot
    └── result-not-likely.png # Not Likely prediction screenshot
```

<blockquote>
⚠️ **Important:** Flask requires the HTML templates to be inside a folder named exactly `templates/`. Keep `index.html` and `result.html` inside this folder.
</blockquote>

---

## 🧠 Machine Learning Workflow

The application uses a pre-trained machine learning model saved with Joblib.

### Prediction Pipeline

1. **User Input:** Collects personal and health information through the web form.
2. **Data Processing:** Converts submitted values into a Pandas DataFrame.
3. **Preprocessing:** Applies the saved preprocessing pipeline, including categorical encoding.
4. **Feature Selection:** Selects the required numerical and encoded features.
5. **Prediction:** The trained classifier generates the prediction.
6. **Result Display:** Flask renders the result page with a clear prediction message.

### Prediction Output

| Model Output | Display Result |
|---|---|
| `1` | Likely |
| `0` | Not Likely |

*These labels represent the model's output, not a confirmed medical diagnosis.*

### Work Type Mapping

Some form labels are converted into the values expected by the trained model.

| Form Label | Model Value |
|---|---|
| Government job | `Govt_job` |
| Children | `children` |
| Never Worked | `Never_worked` |
| Private | `Private` |
| Self-employed | `Self-employed` |

---

## 📝 Input Features

The application uses the following information to generate predictions.

| Feature | Type | Description |
|---|---|---|
| Gender | Categorical | Male / Female |
| Age | Numeric | Age in years |
| Hypertension | Binary | 0 = No, 1 = Yes |
| Heart Disease | Binary | 0 = No, 1 = Yes |
| Ever Married | Categorical | Yes / No |
| Work Type | Categorical | Private, Self-employed, Govt job, Children, Never worked |
| Residence Type | Categorical | Urban / Rural |
| Average Glucose Level | Numeric | Average glucose level (mg/dL) |
| BMI | Numeric | Body Mass Index |
| Smoking Status | Categorical | Never Smoked, Formerly Smoked, Smokes, Unknown |

---

## 🔧 Troubleshooting

| Error / Problem | Solution |
|---|---|
| `TemplateNotFound` | Make sure HTML files are inside `templates/` |
| `FileNotFoundError: model.joblib` | Place the model in the project root |
| UI still looks old | Hard refresh using `Ctrl + Shift + R` |
| Template changes not updating | Enable Flask template auto-reload |
| `No module named flask` | Run `pip install flask` |
| `No module named sklearn` | Run `pip install scikit-learn` |
| Prediction error | Verify that input features match the training pipeline |

### Fix: HTML Changes Not Updating

Add these lines after creating your Flask application:

```python
app.config['TEMPLATES_AUTO_RELOAD'] = True
app.jinja_env.auto_reload = True
```

Restart the Flask server:

```bash
python app.py
```

### Fix: Browser Cache

Use the following keyboard shortcut:

- **Windows/Linux:** `Ctrl + Shift + R`
- **macOS:** `Cmd + Shift + R`

---

## ⚠️ Medical Disclaimer

This project is developed for **educational, research, and machine learning demonstration purposes only**.

- Predictions are based on statistical patterns learned from training data.
- Results may be inaccurate or incomplete.
- This application is not a substitute for professional medical advice, diagnosis, or treatment.
- Never use this application to make medical decisions.
- Always consult a qualified healthcare professional regarding stroke risks or medical concerns.

**If someone experiences possible stroke symptoms, seek emergency medical attention immediately. Do not rely on this application.**

---

## 🗺️ Future Improvements

- [ ] Interactive prediction dashboard
- [ ] Model performance visualization
- [ ] Prediction probability display
- [ ] Downloadable prediction reports
- [ ] User authentication
- [ ] Prediction history (with appropriate privacy safeguards)
- [ ] Improved model accuracy and validation
- [ ] Cloud deployment

---

## 🤝 Contributing

Contributions, suggestions, and improvements are welcome!

1. Fork this repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/new-feature
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add new feature"
   ```

4. Push your branch:

   ```bash
   git push origin feature/new-feature
   ```

5. Open a Pull Request.

---

## 🙌 Acknowledgements

Special thanks to:

- [World Health Organization](https://www.who.int/) — Stroke awareness and health information.
- [Scikit-learn](https://scikit-learn.org/) — Machine learning tools.
- [Flask](https://flask.palletsprojects.com/) — Python web framework.
- [Bootstrap](https://getbootstrap.com/) — Responsive UI framework.
- [Font Awesome](https://fontawesome.com/) — Icons.
- [Google Fonts](https://fonts.google.com/) — Inter typography.

---

<p align="center">
  <strong>🧠 Stroke Prediction Web App</strong>
  <br />
  Built with ❤️ using Python, Flask & Machine Learning.
  <br /><br />
  <sub>Machine Learning for Health Awareness & Education.</sub>
</p>
