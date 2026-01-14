# HYDRA-5 Intelligence System

**Multi-Source Intelligence + Five-Model Crypto Prediction System**

HYDRA-5 is an intelligence-first crypto prediction engine that combines real-time multi-source scraping with intentional confirmation delays and five complementary AI models.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Next.js](https://img.shields.io/badge/next.js-15+-black.svg)

## 🎯 Core Philosophy

- **Speed creates noise, confirmation creates signal**
- **No single model understands all market regimes**
- **Information moves price before indicators**
- **Every prediction must be explainable**

## 🏗️ Architecture Overview

```
Internet Sources (Web, News, Social Media)
        ↓
Continuous Scrapers
        ↓
10-20 Minute Spread Window (Confirmation Delay)
        ↓
MODEL 1: News Spread & Confirmation (XGBoost)
        ↓
MODEL 2: NLP Intelligence Filter (Transformer NLP)
        ↓
Structured Intelligence Signals
        ↓
MODEL 3: LSTM | MODEL 4: TCN | MODEL 5: Time-Series Transformer
        ↓
Meta-Decision Layer
        ↓
Final Probabilities
        ↓
Next.js Dashboard
```

## 🤖 The Five Models

### Model 1: News Spread & Confirmation (XGBoost)
**Purpose**: Decide whether information is real, confirmed, and market-moving

**Features**: Source diversity, spread velocity, sentiment agreement, time persistence

**Output**: Confirmation score, spread velocity, consensus

### Model 2: NLP Intelligence Filter (Transformer)
**Purpose**: Convert confirmed text → structured intelligence

**Responsibilities**: Topic classification, entity extraction, sentiment analysis, impact estimation

### Model 3: LSTM
**Purpose**: Short-medium term memory patterns

**Learns**: Momentum, micro-trends, mean reversion

### Model 4: TCN (Temporal Convolutional Network)
**Purpose**: Structural stability detection

**Learns**: Long-range dependencies, regime identification, volatility structure

### Model 5: Time-Series Transformer
**Purpose**: Global context & regime shifts

**Learns**: Narrative dominance, structural breaks, macro overrides

## 🚀 Quick Start

### Prerequisites

- **Backend**: Python 3.10+, PostgreSQL, Redis
- **Frontend**: Node.js 18+, npm

### Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure environment variables (see backend/README.md)
cp .env.example .env
# Edit .env with your configuration

# Run API server
python run_api.py
```

The backend API will be available at `http://localhost:8000`

### Frontend Setup

```bash
cd frontend

# Install dependencies
npm install

# Set environment variables
export NEXT_PUBLIC_API_URL=http://localhost:8000

# Run development server
npm run dev
```

Visit `http://localhost:3000` to access the dashboard.

### Production Build

```bash
cd frontend
npm run build
npm run start
```

## 📊 Dashboard Features

1. **Overview**: Latest predictions with confidence scores
2. **Intelligence Feed**: Confirmed news and spread metrics
3. **Asset View**: BTC, ETH analysis with model agreement
4. **Model Health**: Individual model performance monitoring

## 🌐 Deployment

### Backend Deployment

The backend can be deployed to any Python hosting service:
- AWS EC2/ECS
- Google Cloud Run
- Heroku
- DigitalOcean App Platform

Ensure PostgreSQL and Redis are configured and accessible.

### Frontend Deployment (Cloudflare Pages)

The frontend is configured for deployment on Cloudflare Pages:

1. **Connect Repository**: Link your GitHub repository to Cloudflare Pages

2. **Build Settings**:
   - Build command: `npm run build`
   - Build output directory: `out`
   - Root directory: `frontend`

3. **Environment Variables**:
   - `NEXT_PUBLIC_API_URL`: Your backend API URL
   - `NODE_VERSION`: `18` or higher

4. **Deploy**: Push to your main branch or use Cloudflare CLI

For detailed Cloudflare deployment instructions, see [frontend/README.md](frontend/README.md)

## 🛠️ Technology Stack

### Backend (Python)
- **Framework**: FastAPI
- **Models**: XGBoost, PyTorch/TensorFlow, HuggingFace Transformers
- **Database**: PostgreSQL
- **Cache**: Redis
- **Scraping**: BeautifulSoup, Scrapy, Tweepy

### Frontend (Next.js)
- **Framework**: Next.js 15+
- **UI**: Tailwind CSS
- **Charts**: Recharts
- **State**: React hooks

## 📁 Project Structure

```
hydra-5-trading-syst/
├── backend/
│   ├── api/                  # FastAPI endpoints
│   ├── models/               # Five AI models
│   │   ├── model1_xgboost/
│   │   ├── model2_nlp/
│   │   ├── model3_lstm/
│   │   ├── model4_tcn/
│   │   └── model5_transformer/
│   ├── meta_decision/        # Ensemble layer
│   ├── scrapers/             # Data collection
│   └── requirements.txt
├── frontend/
│   ├── app/                  # Next.js pages
│   ├── components/           # React components
│   └── package.json
└── README.md
```

## 🔐 Security

- Never commit API keys or credentials
- Use environment variables for sensitive data
- Review [SECURITY.md](SECURITY.md) for security practices

## 📖 Documentation

- [HYDRA5_README.md](HYDRA5_README.md) - Detailed system overview
- [PRD.md](PRD.md) - Product requirements document
- [ARCHITECTURE_DIAGRAM.md](ARCHITECTURE_DIAGRAM.md) - System architecture
- [DASHBOARD_GUIDE.md](DASHBOARD_GUIDE.md) - Dashboard usage guide
- [backend/README.md](backend/README.md) - Backend documentation
- [frontend/README.md](frontend/README.md) - Frontend documentation

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## 📄 License

MIT License - See [LICENSE](LICENSE) file for details

## ⚠️ Disclaimer

HYDRA-5 is an analytical tool for educational and research purposes. It is NOT financial advice. Always do your own research and consult with financial advisors before making investment decisions.

## 💡 Core Principle

> Markets move on **confirmed information**, not **first information**.

HYDRA-5 behaves like an institution-grade intelligence engine, not a retail bot.
