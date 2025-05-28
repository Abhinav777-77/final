"# Scene-Solver" 
Scene-Solver
Scene-Solver is an AI-powered forensic analysis platform that leverages object detection (YOLOv8), vision-language models (like CLIP), and contextual AI reporting to analyze crime scene images and generate automated forensic reports. It includes a modern frontend, robust backend API, and machine learning model integration.

🌐 Features
🔍 Crime Scene Analysis using object detection and image-to-text AI models

🧠 AI-generated Forensic Reports contextualized to the detected elements

🔐 User Authentication with email + OTP support

📊 Case and Report Management

📦 Vector Search via FAISS with embedded text data

🔧 RESTful API Backend using Flask

🖼️ Frontend Interface for user interaction (Vue/React, based on actual implementation)

📁 Project Structure
bash
Copy
Edit
Prj/
├── backend/
│   ├── src/
│   │   ├── app.py               # Flask app entry point
│   │   ├── config/              # Email and DB config
│   │   ├── model/               # AI/ML model logic (e.g., YOLO, CLIP)
│   │   ├── routes/              # Blueprint APIs (auth, analysis, report, etc.)
│   │   └── middleware/          # Custom middleware (if any)
│   ├── crime_dataset.csv        # Sample dataset
│   ├── crime_descriptions_faiss.index  # FAISS vector DB
│   ├── yolov8n.pt               # YOLOv8 object detection model
│   └── requirements.txt         # Python dependencies
├── frontend/                    # Web frontend (Vue or React)
└── README.md
🚀 Getting Started
Backend Setup
Create and activate a virtual environment

bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install dependencies

bash
Copy
Edit
pip install -r Prj/backend/src/requirements.txt
Run the Flask app

bash
Copy
Edit
cd Prj/backend/src
python app.py
Frontend Setup
If React-based (adjust for Vue accordingly):

Navigate to the frontend directory:

bash
Copy
Edit
cd Prj/frontend
Install dependencies:

bash
Copy
Edit
npm install
Run the app:

bash
Copy
Edit
npm start
🧠 AI Model Usage
YOLOv8 (yolov8n.pt) is used for detecting objects in images.

CLIP or other multimodal models are used for understanding context and generating textual summaries.

FAISS is used to store and retrieve semantically similar crime descriptions.

📌 API Endpoints (Sample)
Endpoint	Method	Description
/api/auth/login	POST	OTP-based login
/api/report/generate	POST	Generate AI-based forensic report
/api/analysis/image	POST	Perform object detection & CLIP analysis
/api/case/create	POST	Create new forensic case
/api/invite/send	POST	Invite other analysts via email

⚙️ Configuration
Edit your configuration in config/config.py to set:

Email server details for OTP

MongoDB connection

Flask secret keys

🛡️ Security
OTP login ensures secure user verification

CORS is configured for development ports

Tokens or session handling can be extended for production

📚 Dataset
crime_dataset.csv: Contains crime-related textual descriptions

crime_descriptions_faiss.index: Prebuilt FAISS index for semantic search

📸 Example Use Case
User uploads a crime scene image

Backend detects relevant objects using YOLO

CLIP/AI model analyzes context and generates a forensic summary

Report is saved and can be viewed later with case information

🧪 Testing
Use Postman or any API testing tool to validate backend endpoints.

🧑‍💻 Contributors
[Your Name] - Developer & AI Engineer

[Other Contributors]

📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
