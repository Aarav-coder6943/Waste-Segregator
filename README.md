🌿 Smart Waste Segregation System

AI-powered waste classification using Flask + Ollama + Rule-Based Fallback Intelligence.

This project is a smart environmental assistant that classifies waste items into:

♻️ Recyclable Waste
🟤 Wet Waste
📦 Dry Waste
☣️ Hazardous Waste

It combines:

🤖 Local LLM intelligence using Ollama
🧠 Rule-based fallback AI
🌐 Flask web backend
⚡ Real-time classification API

Basically you built a mini environmental AI agent before half the internet even figured out how to install Python 💀🔥

✨ Features
🤖 AI-powered waste classification
🧠 Local LLM support using Ollama
🔄 Automatic fallback system
🌱 Environmental disposal recommendations
⚠️ Risk-level analysis
🌐 Flask REST API
⚡ Fast keyword-based backup classifier
🛡️ Input validation & error handling
🏠 Fully offline capable
🛠️ Tech Stack
Python
Flask
Ollama
llama3.1
Regex
Requests
JSON APIs
📂 Project Structure
Smart-Waste-AI/
│
├── templates/
│   └── frontend_wasteAI.html
│
├── app.py
└── README.md
🚀 How It Works

The system follows a hybrid AI pipeline:

User Input
    ↓
Ollama LLM Classification
    ↓
If Ollama Fails
    ↓
Rule-Based Fallback System
    ↓
Waste Category + Disposal Advice + Risk Analysis

This makes the system:

Reliable
Fast
Offline-capable
More fault tolerant

Honestly this is lowkey production-style architecture 😭

♻️ Waste Categories
Category	Description
Wet Waste	Organic biodegradable waste
Dry Waste	Non-biodegradable non-hazardous waste
Hazardous Waste	Toxic or dangerous materials
Recyclable Waste	Materials that can be reprocessed
🤖 AI Classification System

The project uses:

Ollama
Alibaba Cloud

with:

OLLAMA_MODEL = "llama3.1"

The LLM receives structured prompts and returns:

Waste category
Disposal recommendation
Risk level
Environmental reasoning
🧠 Prompt Engineering

The model is forced into a strict structured format for reliable parsing.

This reduces:

hallucinations
random formatting
inconsistent outputs

Actually smart af because most beginner AI apps completely ignore this 💀

⚡ Fallback Intelligence System

If Ollama is unavailable:

The app automatically switches to a keyword-based classifier.

This ensures:

Offline reliability
Fast response times
No total system failure
🧮 Classification Logic

Keyword scoring determines fallback categories:

score(category)=∑keyword matches

The category with the highest score becomes the prediction.

🌐 Flask API Routes
Home Route
@app.route("/")

Loads the frontend interface.

Classification API
@app.route("/classify", methods=["POST"])

Accepts JSON input and returns:

category
disposal method
risk level
reasoning
source used
📦 Example API Response
{
  "category": "Wet Waste",
  "disposal": "Compost it in a home compost bin.",
  "risk": "Low",
  "reason": "This is biodegradable organic matter.",
  "source": "ollama"
}
⚙️ Installation
Clone Repository
git clone https://github.com/Aarav-coder6943/Waste-segregator.git
cd smart-waste-ai
Install Dependencies
pip install flask requests
🤖 Install Ollama

Download:

Ollama Official Website

Then pull the model:

ollama pull llama3.1
▶️ Usage

Run the Flask app:

python app.py

Open:

http://127.0.0.1:5000
📸 Example Inputs
Input	Output
Banana Peel	Wet Waste
Plastic Bottle	Recyclable Waste
Battery	Hazardous Waste
Cardboard Box	Dry Waste
🧠 Input Validation

The app prevents:

Empty requests
Extremely long prompts
Invalid formatting

This improves:

Security
API reliability
LLM stability
📈 Future Improvements
📷 Image-based waste detection
🧠 Vision-language AI models
🌍 Multi-language support
📱 Mobile application
♻️ Recycling center integration
☁️ Cloud deployment
📊 Waste analytics dashboard
🛰️ Smart city integration
⚠️ Limitations
Keyword fallback is less accurate than LLM classification
Requires Ollama setup for full AI capability
Some waste items may belong to multiple categories depending on local regulations
💡 Inspiration

Inspired by:

Smart city waste systems
Sustainable technology
AI environmental assistants
Offline local LLM applications

Because garbage sorting manually in 2026 feels illegal at this point 😭


🙌 Acknowledgements
Flask
Ollama
Alibaba Cloud
⭐ Support

If this project made you feel like you accidentally built eco-friendly Jarvis, give the repo a star ⭐
