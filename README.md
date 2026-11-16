# 🌿 Green AI Cloud Scheduler

A carbon-aware AI cloud workload scheduler and interactive Streamlit sustainability dashboard that optimizes compute routing across global data centers to minimize carbon emissions and operational costs.

## 📂 Project Structure

- **`generate_data.py`**: Generates synthetic workload traffic, regional carbon intensity, and energy pricing datasets (`traffic_data.csv`).
- **`model.py`**: Defines the optimization model for carbon-aware and cost-aware workload scheduling.
- **`decision_engine.py`**: Executes routing decisions across data center regions and outputs `decisions.csv`.
- **`evaluate.py`**: Evaluates baseline vs. optimized performance, generating `results_summary.csv` and `comparison_chart.png`.
- **`dashboard.py`**: Interactive Streamlit web application with authentication, sidebar navigation, scenario comparisons, and step-by-step routing logs.

---

## 💻 How to Run Locally on Your Laptop

### 1. Prerequisites
Make sure you have **Python 3.9+** installed on your system.

### 2. Clone or Download the Repository
Using Git:

    git clone https://github.com/Suhani00796/green-optimizer.git
    cd green-optimizer

*(Or click **Code → Download ZIP** on this GitHub page, extract the folder, and open a terminal or PowerShell inside it.)*

### 3. Install Required Packages

    pip install streamlit pandas numpy matplotlib

*(On Windows, if `pip` is not recognized, run `py -m pip install streamlit pandas numpy matplotlib`.)*

### 4. Re-run the Data & Optimization Pipeline (Optional)
Pre-generated results (`decisions.csv`, `results_summary.csv`, and `comparison_chart.png`) are already included in this repository. To regenerate them from scratch, run:

    python generate_data.py
    python decision_engine.py
    python evaluate.py

### 5. Launch the Dashboard

    streamlit run dashboard.py

*(On Windows, run `py -3.12 -m streamlit run dashboard.py` if `streamlit` is not in your system PATH.)*

### 6. Log In to the Portal
Once the app opens in your browser (usually at `http://localhost:8501`), sign in using the default demo credentials or create a new session account under the **Sign Up** tab:
- **Username:** `admin`
- **Password:** `admin123`
