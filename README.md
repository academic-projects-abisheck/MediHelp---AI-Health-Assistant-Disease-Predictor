# MediHelp 🏥 — AI-Powered Disease Prediction & Virtual Health Companion

**MediHelp** is an intelligent, full-stack healthcare web application designed to evaluate patient health indicators, predict potential medical risks (Cardiovascular, Diabetes, and Respiratory), and provide conversational medical guidance using a custom-integrated Gemini AI chatbot. 

This repository represents the culmination of an intensive **6-day engineering sprint** completed during my **4th semester**, focusing on machine learning implementation, database security, and responsive UI design.

---

## 🚀 Key Features Built in 6 Days

*   **🧠 Tri-Core Disease Prediction Engine:** Integrates three pre-trained machine learning classification models loaded via `joblib`:
    *   **Cardiovascular Risk Classifier:** Analyzes clinical indicators including systolic/diastolic blood pressure, cholesterol, glucose, age, and activity level.
    *   **Diabetes Risk Classifier:** Utilizes age, hypertension, heart disease history, BMI, HbA1c, blood glucose, and a dynamically computed `glucose_bmi_ratio`.
    *   **Respiratory Condition Evaluator:** Assesses lifestyle indicators (smoking history, alcohol consumption) and clinical symptoms (chest pain, wheezing, cough, fatigue).
*   **🤖 Native Gemini AI Health Assistant:** Integrated Google's `gemini-3.1-flash-lite` API to provide an empathetic chatbot optimized for general medical inquiries, preventative health advice, and site navigation. Includes:
    *   A custom context-aware system prompt.
    *   Active conversational history support (maintaining state across messages).
    *   Pre-configured quick-query suggested prompts.
*   **🔒 Secure User Authentication & Management:** Built a complete user registration and login system backed by **MongoDB**. Passwords are encrypted using salted cryptographic hashing (`werkzeug.security`).
*   **📱 Glassmorphic Frontend & UI:** Designed a responsive user interface with vanilla CSS using glassmorphism aesthetics, interactive card menus, form input validation alerts, and asynchronous request loading indicators.

---

## 📈 Learnings & Engineering Outcomes

Developing a production-ready medical helper tool in a single week required tackling several engineering challenges:

1.  **Seamless Backend-to-Frontend Integration:** Developed clean asynchronous client-server communication using the Javascript Fetch API, communicating with Flask REST endpoints. Kept page loads fast and highly interactive.
2.  **Machine Learning Lifecycle in Web Apps:** Gained experience in loading serialized model files (`.pkl`), preprocessing raw form data to feed numpy arrays and pandas dataframes, and converting numerical outputs into patient-friendly risk levels.
3.  **Secure Environment Configurations:** Decoupled sensitive credentials (database strings, API keys, session secrets) from the source code by managing them in `.env` configurations.
4.  **Generative AI Prompts & Integration:** Learned to structure custom API requests directly to Google's Gemini endpoint, handling conversation state lists and tailoring system prompts for high-responsibility domains (medical/health information).
5.  **Clean Code & Dynamic Paths:** Optimized hardcoded local development paths to relative pathways, resolving OS differences and ensuring the repository is fully portable.

---

## 🛠️ Tech Stack Used

*   **Backend:** Python, Flask
*   **Database:** MongoDB, Flask-PyMongo
*   **Machine Learning:** Scikit-Learn, Pandas, NumPy, JobLib
*   **APIs:** Google Gemini API (`gemini-3.1-flash-lite`) via custom HTTP POST integrations
*   **Frontend:** HTML5, Vanilla CSS, Vanilla JavaScript, Remix Icons, Google Fonts

---

## ⚙️ Installation & Setup

1.  **Clone the Repository:**
    ```bash
    git clone https://github.com/your-username/MediHelp.git
    cd MediHelp
    ```
2.  **Install Python Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Configure Environment Variables:**
    Create a `.env` file in the root directory:
    ```env
    GEMINI_API_KEY=your_gemini_api_key_here
    MONGO_URI=mongodb://localhost:27017/usersdb
    SECRET_KEY=your_custom_flask_secret_key
    ```
4.  **Run the Server:**
    Make sure MongoDB is active on your machine, then run:
    ```bash
    python app.py
    ```
    Access the app at **[http://127.0.0.1:5000](http://127.0.0.1:5000)**!



## 📸 User Interface Screenshots


#### Home Page - Hero Section
<img width="1627" height="862" alt="image" src="https://github.com/user-attachments/assets/8c37aaee-92b0-428e-8f99-947a3abe7c09" />


#### Services Providing 

<img width="1592" height="663" alt="image" src="https://github.com/user-attachments/assets/abb31103-cb86-4185-bd7c-b0212af2ba1c" />


#### Home Page - General Info. & Footer
<img width="832" height="851" alt="image" src="https://github.com/user-attachments/assets/48b1609f-3df9-4c1f-a0cd-10e4bd32005b" />


#### Chatbot MediHelp
<img width="956" height="786" alt="image" src="https://github.com/user-attachments/assets/af51fbbc-fadb-4d9e-a424-e2df28ad4ae2" />



#### Personalized Review 
<img width="703" height="862" alt="image" src="https://github.com/user-attachments/assets/5ec96102-908d-42ab-a9af-836e34353e53" />


#### Medical Diagnostic Assistant
<img width="1708" height="807" alt="image" src="https://github.com/user-attachments/assets/87fd168a-771f-46f5-8695-d97194507a38" />

#### Health Assessment Page
<img width="588" height="815" alt="image" src="https://github.com/user-attachments/assets/ff10fe3f-53e6-45c1-8b9f-e598310b0e49" />
