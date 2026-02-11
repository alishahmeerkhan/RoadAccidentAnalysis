# 🚦 Road Accident Analysis & Insights System

An interactive desktop application designed to explore and analyze road accident trends in Pakistan. This tool automates the process of data cleaning, provides various statistical visualizations, and leverages **Google's Gemini AI** to interpret data patterns and provide actionable safety insights.

---

## ✨ Key Features
- **Interactive GUI:** A custom-styled Tkinter interface featuring a dark theme and intuitive navigation menus.
- **Automated Data Cleaning:** - Handles missing values in critical columns like `responsetime`.
    - Drops redundant features such as `EcNumber` and `CallTime`.
    - Engineers new features like `Vehicles Involved` mapping and `ACCLASS Severity` levels.
- **Dynamic Visualizations:** Integrated Matplotlib plots within the Tkinter window, including:
    - **Scatter Plots:** To find correlations between time, age, and severity.
    - **Histograms:** To view frequency distributions of accidents over months or years.
    - **Line Graphs:** To track injury types and patient status trends.
    - **Pie Charts:** To visualize weather, lighting, and gender distributions.
- **AI-Powered Insights:** Uses **Gemini 2.5 Flash** to analyze dataset samples and answer natural language queries directly through the app.
- **Data Source:** Pakistani Road Traffic Accident (RTA) dataset from Kaggle. [https://www.kaggle.com/datasets/irakozekelly/road-traffic-accident-dataset-pakistan]

---

## 🛠️ Tech Stack
- **Language:** Python 3.13+
- **Data Analysis:** Pandas
- **Visualization:** Matplotlib
- **AI Integration:** Google Generative AI SDK (`google-generativeai`)
- **GUI Framework:** Tkinter

---

## 📂 Project Structure
- `Road Accident Analysis.ipynb`: The primary source file containing the application logic, data cleaning pipeline, and GUI implementation.
- `RTA.csv`: The dataset containing road accident records (required for execution).
- `.venv/`: Python virtual environment containing necessary dependencies.

---

## 🚀 Getting Started

### Prerequisites
1.  **Get a Gemini API Key:** Visit [Google AI Studio](https://aistudio.google.com/) to generate a free API key.
2.  **Install Dependencies:**
    ```bash
    pip install pandas matplotlib google-generativeai
    ```

### Installation & Usage
1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/alishahmeerkhan/RoadAccidentAnalysis.git](https://github.com/alishahmeerkhan/RoadAccidentAnalysis.git)
    ```
2.  **Setup API Key:** Open the project file and replace the `API_KEY` variable in the `getInsights` function with your actual key.
    > **Note:** For security, it is recommended to use environment variables instead of hardcoding the key.
3.  **Run the App:** Execute the script to launch the Home Page.

---

## 📊 Logic & Methodology
1.  **Data Loading:** The app reads `RTA.csv` using Pandas.
2.  **Preprocessing:** - Rows with missing response times are filled with the mean value.
    - A mapping function translates categorical accident severity (e.g., "Fatal", "Minor") into numerical ranks (1-5) for plotting.
3.  **Visualization:** The `FigureCanvasTkAgg` backend is used to embed Matplotlib figures directly into the Tkinter window.
4.  **AI Analysis:** The app sends a 50-row data sample along with the user's prompt to Gemini for contextual analysis.

---

## 👤 Author
**Shahmeer Khan** *Student at FAST NUCES, Pakistan*

---
