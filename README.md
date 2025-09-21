# TruthFinder AI

![TruthFinder AI](https://img.shields.io/badge/TruthFinder-AI-blue?style=for-the-badge&logo=brain)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![React](https://img.shields.io/badge/React-18.2.0-blue?style=for-the-badge&logo=react)
![Flask](https://img.shields.io/badge/Flask-2.0+-green?style=for-the-badge&logo=flask)

> **Your AI-powered media literacy co-pilot** - Analyze articles for bias, manipulation, and trustworthiness using advanced AI technology.

## 🎯 Overview

TruthFinder AI is a prototype system built during the GenAI Exchange Hackathon that detects, analyzes, and explains misinformation in text with human-in-the-loop review capabilities. The application combines the power of Google's Gemini AI with a modern React frontend to provide comprehensive article analysis.

## ✨ Features

- **🔍 Article Analysis**: Extract and analyze content from any web article URL
- **🤖 AI-Powered Detection**: Uses Google Gemini AI for sophisticated content analysis
- **📊 Trust Scoring**: Provides a 1-10 trustworthiness score for articles
- **⚠️ Manipulation Detection**: Identifies manipulative techniques and bias patterns
- **📈 Sensationalism Analysis**: Measures sensationalism levels in content
- **🎨 Modern UI**: Beautiful, responsive interface built with React and Tailwind CSS
- **🔄 Real-time Processing**: Fast analysis with loading states and error handling

## 🏗️ Architecture

```
TruthFinder-AI/
├── backend/                 # Flask API server
│   ├── api.py              # Main API endpoints
│   └── requirements.txt    # Python dependencies
├── frontend/               # React application
│   ├── src/
│   │   ├── TruthFinderApp.js  # Main application component
│   │   ├── App.js             # App wrapper
│   │   └── index.js           # Entry point
│   ├── package.json        # Node.js dependencies
│   └── tailwind.config.js  # Tailwind CSS configuration
└── README.md              # This file
```

## 🚀 Quick Start

### Prerequisites

- **Python 3.8+**
- **Node.js 16+**
- **Google AI API Key** (for Gemini)

### 1. Clone the Repository

```bash
git clone https://github.com/genaiexchangegit/TruthFinder-AI.git
cd TruthFinder-AI
```

### 2. Backend Setup

```bash
# Navigate to backend directory
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Set environment variable for Google AI API
export GOOGLE_API_KEY="your_api_key_here"
# On Windows:
set GOOGLE_API_KEY=your_api_key_here

# Run the Flask server
python api.py
```

The backend will be available at `http://127.0.0.1:5000`

### 3. Frontend Setup

```bash
# Navigate to frontend directory (in a new terminal)
cd frontend

# Install dependencies
npm install

# Start the development server
npm start
```

The frontend will be available at `http://localhost:3000`

## 🔧 API Endpoints

### `POST /analyze`
Analyzes an article from a given URL.

**Request Body:**
```json
{
  "url": "https://example.com/article"
}
```

**Response:**
```json
{
  "title": "Article Title",
  "summary": "Brief summary of the article",
  "toneAnalysis": "Analysis of the article's tone",
  "sensationalismScore": 7,
  "manipulativeTechniques": [
    {
      "technique": "Fear mongering",
      "explanation": "Uses alarming language to create fear"
    }
  ],
  "trustScore": 6,
  "finalVerdict": "Overall assessment of the article"
}
```

### `GET /health`
Health check endpoint.

**Response:**
```json
{
  "status": "healthy"
}
```

## 🛠️ Technology Stack

### Backend
- **Flask**: Web framework for Python
- **Google Generative AI**: AI analysis using Gemini model
- **Newspaper3k**: Article extraction and parsing
- **Flask-CORS**: Cross-origin resource sharing

### Frontend
- **React 18.2.0**: Modern React with hooks
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Beautiful icon library
- **Create React App**: Development tooling

## 📊 Analysis Features

### Trust Score (1-10)
- **8-10**: Highly trustworthy content
- **6-7**: Moderately trustworthy with some concerns
- **4-5**: Questionable content with significant issues
- **1-3**: Low trustworthiness, likely misinformation

### Sensationalism Score (1-10)
- **1-3**: Low sensationalism, factual reporting
- **4-6**: Moderate sensationalism
- **7-8**: High sensationalism, clickbait elements
- **9-10**: Extreme sensationalism, likely misleading

### Manipulative Techniques Detection
- Fear mongering
- Emotional manipulation
- Cherry-picking data
- False equivalencies
- Loaded language
- And more...

## 🔑 Environment Variables

Create a `.env` file in the backend directory:

```env
GOOGLE_API_KEY=your_google_ai_api_key_here
```

## 🚀 Deployment

### Backend Deployment
The Flask app can be deployed using Gunicorn:

```bash
gunicorn -w 4 -b 0.0.0.0:5000 api:app
```

### Frontend Deployment
Build the React app for production:

```bash
cd frontend
npm run build
```

The built files will be in the `build/` directory.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Hackathon

This project was built during the **GenAI Exchange Hackathon** as a prototype system for detecting and analyzing misinformation in media content.

## 🙏 Acknowledgments

- **Google AI** for providing the Gemini API
- **GenAI Exchange** for organizing the hackathon
- **React** and **Flask** communities for excellent documentation
- **Tailwind CSS** for the beautiful design system

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/genaiexchangegit/TruthFinder-AI/issues) page
2. Create a new issue with detailed information
3. Include error messages and steps to reproduce

---

**Built with ❤️ for media literacy and truth in the digital age**
