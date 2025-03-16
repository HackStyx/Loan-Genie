# Loan Genie 🧞‍♂️

<div align="center">

[![React](https://img.shields.io/badge/React-18.2.0-blue.svg)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.7.2-blue.svg)](https://www.typescriptlang.org/)
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109.2-green.svg)](https://fastapi.tiangolo.com/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.3.0-38B2AC.svg)](https://tailwindcss.com/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.3.2-orange.svg)](https://scikit-learn.org/)
[![Sarvam AI](https://img.shields.io/badge/Sarvam%20AI-Translation-blue.svg)](https://sarvam.ai/)
[![Supabase](https://img.shields.io/badge/Supabase-Auth%20&%20Storage-green.svg)](https://supabase.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A modern, AI-powered loan prediction and management system with multi-language support.

</div>

## ✨ Features

### 🤖 Intelligent Loan Assessment
- **Smart Prediction Engine**: Leverages advanced machine learning to analyze your loan eligibility in real-time
- **Confidence Scoring**: Get detailed insights into your application's approval probability
- **Personalized Recommendations**: Receive tailored suggestions to improve your loan application
- **Instant Results**: No waiting - get your loan eligibility assessment in seconds

### 🌐 Seamless Multi-Language Experience
- **11 Indian Languages**: Access the platform in your preferred language
- **Real-Time Translation**: Powered by Sarvam AI's cutting-edge translation technology
- **Natural Language Processing**: Understand complex financial terms in your native language
- **Instant Language Switching**: Switch languages without losing your progress

### 🔒 Enterprise-Grade Security
- **Bank-Level Authentication**: Secure login powered by Supabase
- **Protected Data**: Your sensitive information is encrypted and secure
- **Secure Document Handling**: Safe upload and storage of your documents
- **Role-Based Access**: Different access levels for users and administrators

### 💫 Modern User Experience
- **Stunning Animations**: Smooth transitions and interactions powered by Framer Motion
- **Responsive Design**: Perfect experience on any device, from mobile to desktop
- **Dark Mode**: Eye-friendly interface with dark mode support
- **Interactive Components**: Engaging UI elements that make the process enjoyable

### 📊 Comprehensive Financial Dashboard
- **Real-Time Tracking**: Monitor your loan application status in real-time
- **Smart Analytics**: Visual insights into your financial profile
- **Document Management**: Easy upload and organization of required documents
- **Financial Education**: Access to curated financial literacy resources

## 🌐 Sarvam AI Integration

<details>
<summary><h3>Text Translation API</h3></summary>

- **Endpoint**: `POST /translate`
- **Purpose**: Translates text between different languages
- **Supported Languages**: 11 Indian languages including Hindi, Tamil, Telugu, Malayalam, Kannada, Bengali, Marathi, Gujarati, Punjabi, Odia, and Assamese
- **Rate Limits**: 1000 requests per minute
- **Response Time**: < 500ms
- **Error Handling**: Retries on 5xx errors with exponential backoff

</details>

<details>
<summary><h3>Text Transliteration API</h3></summary>

- **Endpoint**: `POST /transliterate`
- **Purpose**: Converts text between different scripts
- **Supported Scripts**: Devanagari, Tamil, Telugu, Malayalam, Kannada, Bengali
- **Rate Limits**: 2000 requests per minute
- **Response Time**: < 300ms
- **Error Handling**: Automatic script detection

</details>

<details>
<summary><h3>Speech to Text API</h3></summary>

- **Endpoint**: `POST /speech-to-text`
- **Purpose**: Converts spoken audio to text
- **Supported Audio Formats**: WAV, MP3, M4A
- **Maximum Audio Length**: 5 minutes
- **Supported Languages**: All 11 Indian languages
- **Rate Limits**: 100 requests per minute
- **Response Time**: < 2 seconds for 1-minute audio

</details>

<details>
<summary><h3>Speech to Text Translation API</h3></summary>

- **Endpoint**: `POST /speech-to-text-translate`
- **Purpose**: Converts speech to text and translates it
- **Supported Audio Formats**: WAV, MP3, M4A
- **Maximum Audio Length**: 5 minutes
- **Supported Language Pairs**: All combinations of 11 Indian languages
- **Rate Limits**: 50 requests per minute
- **Response Time**: < 3 seconds for 1-minute audio

</details>

<details>
<summary><h3>Text to Speech API</h3></summary>

- **Endpoint**: `POST /text-to-speech`
- **Purpose**: Converts text to natural-sounding speech
- **Supported Languages**: All 11 Indian languages
- **Voice Options**: Multiple voices per language
- **Audio Format**: MP3, WAV
- **Rate Limits**: 500 requests per minute
- **Response Time**: < 1 second for 100 characters

</details>

## 🛠️ Tech Stack

### Frontend
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **State Management**: React Context
- **Routing**: React Router v6
- **Animations**: Framer Motion
- **UI Components**: Custom components with Tailwind
- **Authentication**: Supabase Auth
- **File Upload**: React Dropzone
- **Notifications**: React Hot Toast

### Backend
- **Framework**: FastAPI
- **ML Framework**: scikit-learn
- **Database**: Supabase
- **File Storage**: Supabase Storage

### Machine Learning
- **Model**: Random Forest Classifier
- **Preprocessing**: StandardScaler
- **Features**:
  - Age
  - Experience
  - Income
  - Family size
  - Credit card spending
  - Education level
  - Mortgage value
  - Account types
  - Online banking usage

## 🚀 Getting Started

### Prerequisites
- Node.js (v16 or higher)
- Python (v3.8 or higher)
- npm or yarn
- Supabase account
- Sarvam AI API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/HackStyx/loan-genie.git
   cd loan-genie
   ```

2. **Install Frontend Dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Install Python Dependencies**
   ```bash
   cd "Loan Prediction model"
   pip install -r requirements.txt
   ```

4. **Environment Setup**
   ```bash
   # Frontend
   cp .env.example .env
   
   # Backend
   cd "Loan Prediction model"
   cp .env.example .env
   ```

5. **Start Development Servers**
   ```bash
   # Terminal 1 - Frontend
   npm run dev
   
   # Terminal 2 - Backend
   cd "Loan Prediction model"
   python api.py
   ```

## 🔧 Configuration

### Frontend Environment Variables
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
VITE_GROQ_API_KEY=your_groq_api_key
VITE_SARVAM_API_KEY=your_sarvam_api_key
```

### Backend Environment Variables
```env
ALLOWED_ORIGINS=http://localhost:5173,https://your-production-domain.com
MODEL_PATH=loan_prediction_model.joblib
SCALER_PATH=scaler.pkl
HOST=0.0.0.0
PORT=8000
DEBUG=False
SECRET_KEY=your-secret-key-here
API_KEY=your-api-key-here
```

## 📁 Project Structure

```
loan-genie/
├── src/
│   ├── components/
│   │   ├── ui/                    # Reusable UI components
│   │   │   ├── Button.tsx
│   │   │   ├── Input.tsx
│   │   │   ├── Card.tsx
│   │   │   └── ...
│   │   ├── Dashboard.tsx          # Main dashboard component
│   │   ├── LoanApplication.tsx    # Loan application form
│   │   ├── LoanEligibility.tsx    # Loan eligibility checker
│   │   ├── SignUp.tsx            # User registration
│   │   ├── Login.tsx             # User authentication
│   │   └── Profile.tsx           # User profile management
│   ├── contexts/                  # React contexts
│   │   ├── AuthContext.tsx       # Authentication context
│   │   └── ThemeContext.tsx      # Theme management
│   ├── lib/                      # Utility functions
│   │   ├── supabase.ts          # Supabase client setup
│   │   ├── api.ts               # API integration
│   │   └── utils.ts             # Helper functions
│   ├── types/                    # TypeScript type definitions
│   │   └── index.ts
│   ├── styles/                   # Global styles
│   │   └── globals.css
│   ├── App.tsx                   # Main application component
│   └── main.tsx                  # Application entry point
├── Loan Prediction model/         # Backend ML model
│   ├── api.py                    # FastAPI application
│   ├── loan_predictor.py         # ML model implementation
│   ├── requirements.txt          # Python dependencies
│   ├── loan_prediction_model.joblib  # Trained model
│   └── scaler.pkl               # Feature scaler
├── public/                       # Static assets
│   ├── images/
│   └── favicon.ico
├── .env.example                  # Environment variables template
├── .gitignore                    # Git ignore rules
├── index.html                    # HTML entry point
├── package.json                  # Frontend dependencies
├── tsconfig.json                 # TypeScript configuration
├── vite.config.ts               # Vite configuration
├── tailwind.config.js           # Tailwind CSS configuration
└── README.md                     # Project documentation
```

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Supabase](https://supabase.com/) for authentication and storage
- [Sarvam AI](https://sarvam.ai/) for translation services
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [FastAPI](https://fastapi.tiangolo.com/) for the backend framework
