# ❤️ HeartHealth AI | Clinical Neural Diagnostics

**HeartHealth AI** is a high-fidelity web application that leverages **Logistic Regression** and **Explainable AI (XAI)** to provide clinical-grade cardiovascular risk assessments. Trained on the UCI Heart Disease dataset, the system achieves **~86% accuracy** in real-time inference while providing users with interactive 3D anatomy and live environmental data integration.

---

## 🚀 Key Features

* **Neural Diagnostics:** Real-time risk classification (Low, Mild, Moderate, High) using an optimized Logistic Regression pipeline.
* **Explainable AI (XAI):** A custom **Feature Impact Analysis** engine that visualizes which biological factors (Age, Cholesterol, BP, etc.) most influenced the model's decision.
* **3D Clinical Anatomy:** Native WebGL rendering of the human heart and cardiovascular system using Google’s `model-viewer`.
* **Live Environmental Risk:** Integration with the **Open-Meteo API** to factor in atmospheric PM2.5 levels, adding environmental context to cardiac health.
* **Holographic UI:** A futuristic "Medical Terminal" aesthetic featuring glassmorphism, live EKG pulse animations, and a scanning matrix.
* **Clinical Report Engine:** A print-ready interface allowing users to export their diagnostic summary and neural insights as a professional PDF report.

---

## 🛠️ Technical Stack

* **Frontend:** HTML5, CSS3 (Glassmorphism), Bootstrap 5, Chart.js.
* **Backend:** Flask (Python).
* **Machine Learning:** Scikit-Learn (Logistic Regression), NumPy, Pandas.
* **3D Assets:** GLB Models (Google Model Viewer).
* **Deployment:** Vercel (Serverless Functions).

---

## 📊 Model Pipeline & Logic

The model was meticulously trained to handle real-world clinical data and avoid common ML pitfalls:

1.  **Linear Extrapolation:** By moving from SVC to **Logistic Regression**, the model accurately understands that lower age correlates with lower risk, even for ages below the training distribution.
2.  **Feature Selection:** Dropped non-predictive variables (like `id`) to prevent data leakage and focused on 7 high-impact variables available in the UI.
3.  **Probability Mapping:** Instead of a simple binary output, the system calculates probability distributions to assign clinical "Categories" (0-3).
4.  **XAI Coefficients:** The app extracts model coefficients to explain which features "pushed" the probability higher or lower for each specific user.

---

## 📦 Installation & Local Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/heart-health-ai.git](https://github.com/yourusername/heart-health-ai.git)
   cd heart-health-ai
