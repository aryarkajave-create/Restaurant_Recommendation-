🍽️ Essenza Dining: Content-Based Restaurant Recommender

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-Backend-black?style=for-the-badge&logo=flask)
![Scikit-Learn](https://img.shields.io/badge/Machine_Learning-Scikit_Learn-orange?style=for-the-badge&logo=scikit-learn)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-Light_Mode-38B2AC?style=for-the-badge&logo=tailwind-css)

*Essenza Dining* is an intelligent, web-based recommendation engine designed to curate personalized dining experiences in Bangalore. 

Moving beyond generic top-10 lists, this project leverages *Natural Language Processing (NLP)* to analyze unstructured customer reviews and quantitative metrics (cuisine type, cost, ratings). By processing these features through a custom TF-IDF vectorization engine, it provides highly accurate, taste-matched restaurant recommendations instantly.

---

🚀 Key Features

*⚡ Real-Time Engine:* Optimized Flask backend computes cosine similarity across thousands of data points in milliseconds.
*🔍 Smart Auto-Complete:** Features a dynamic, AJAX-powered search bar that fetches database matches as the user types, complete with full keyboard navigation (Up/Down/Enter).
*🧠 Advanced NLP Model:** Powered by Scikit-Learn's `TfidfVectorizer` to extract semantic meaning from customer reviews, ignoring irrelevant stop words via `NLTK`.
*🎨 Premium UI/UX:** A sleek, modern "Light Mode" interface built entirely with **Tailwind CSS**, featuring custom-styled data dashboards, hover states, and soft glassmorphism.
*📊 Pre-Trained Efficiency:** The heavy mathematical matrix is pre-compiled via Jupyter Notebook into a `.pkl` file, resulting in zero-lag user queries.

---

📂 Project Structure

This architecture strictly adheres to the SmartInternz workspace requirements for model training and deployment:

```text
Restaurant_Recommendation_System/
│
├── Dataset/
│   └── Dataset.txt                         # Compressed raw dataset
│
├── Document/
│   └── RESTAURANT_RECOMMENDATION_SYSTEM.docx                   # Final Project Report
│
├── Model/
│   └── Restaurant_Recommendation_System.ipynb               # Backup of analysis notebook
│
├── Flask/
│   │   ├── templates/
│   │              ├── index.html                         # Premium landing page
│   │              ├── web.html                           # Auto-complete search interface
│   │              └── result.html                        # Formatted data output dashboard
│   │
│   ├── app1.py                                                                                            # Main Flask Web Server
│   ├── Restaurant_Recommendation_System.ipynb                # Primary Training Script (EDA & Model)
│
├── requirements.txt               
 └── README.md  

 ⚙️ Installation & Setup

 1. Prerequisites
Ensure you have Python installed on your system. Install all required dependencies using:
```pip install -r requirements.txt

 2. Train the Model (Jupyter Notebook)
Before booting the web server, you must clean the raw dataset and generate the trained machine learning matrix.

Open your terminal and navigate to the Flask directory.

Ensure your extracted zomato.csv file is inside the Flask folder.

Open Restaurant_Recommendation_System.ipynb using Jupyter or VS Code.

Run all cells sequentially to perform Exploratory Data Analysis (EDA) and train the model.

Verify that restaurant.pkl and restaurant1.csv have successfully generated in your Flask folder.

 3. Run the Application
Start the local server by executing the main Flask application:
python app1.py

 4. Access the Interface
Open your preferred web browser and navigate to the local server address:
http://127.0.0.1:5000/

🧠 Architectural Workflow
Dynamic Input: As the user types into the interface, an AJAX request queries the backend to suggest matching restaurant names, ensuring accurate data entry.

Vectorization & Inference: Upon submission, the application loads the restaurant.pkl file, which contains a pre-computed matrix comparing the TF-IDF (Term Frequency-Inverse Document Frequency) of all restaurant reviews.

Similarity Scoring: The system identifies the index of the target restaurant and calculates the top 10 closest matches based on Cosine Similarity scores.

Data Presentation: The Pandas DataFrame is formatted dynamically into a clean, Tailwind-styled HTML table and rendered on the results dashboard.

📝 License & Credits
This project is developed for educational purposes as part of the SmartInternz Applied Data Science Internship Program.


Developed by 
Arya Rupal Kajave
