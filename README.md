"# CI/CD Automation Tool

An autonomous CI/CD monitoring and remediation system with MongoDB backend and React frontend.

## Features

- 🤖 Automated GitHub Actions monitoring
- 🔧 Intelligent failure diagnosis and remediation
- 📊 Real-time dashboard with statistics
- 🗄️ MongoDB database for persistent storage
- ⚡ FastAPI backend with async support
- 💻 Modern React frontend with Vite

## Quick Start

### Prerequisites

- Python 3.11+
- Node.js 18+
- MongoDB (local or Atlas)
- GitHub Token
- Groq API Key

### Local Development

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd CICDAgent
   ```

2. **Setup Backend**
   ```bash
   cd backend
   python -m venv venv
   source venv/bin/activate  # On Windows: .\venv\Scripts\activate
   pip install -r requirements.txt
   
   # Copy environment variables
   cp .env.example .env
   # Edit .env with your credentials
   
   # Run backend
   python main.py
   ```

3. **Setup Frontend**
   ```bash
   cd frontend
   npm install
   
   # Copy environment variables
   cp .env.example .env
   # Edit .env with backend URL
   
   # Run frontend
   npm run dev
   ```

4. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:8000
   - API Docs: http://localhost:8000/docs

## Deployment

### Deploy to Render

See [DEPLOYMENT.md](DEPLOYMENT.md) for detailed instructions on deploying to Render.

Quick steps:
1. Push code to GitHub
2. Connect repository to Render
3. Configure environment variables
4. Deploy using `render.yaml` blueprint

### Environment Variables

**Backend:**
- `MONGODB_URL` - MongoDB connection string
- `GITHUB_TOKEN` - GitHub personal access token
- `GROQ_API_KEY` - Groq API key

**Frontend:**
- `VITE_API_URL` - Backend API URL

## Architecture

```
├── backend/          # FastAPI backend
│   ├── main.py      # Main application
│   ├── src/
│   │   ├── agent/   # Monitoring agent logic
│   │   ├── llm/     # LLM client
│   │   └── utils/   # Utilities
│   └── config.yaml  # Configuration
│
└── frontend/        # React + Vite frontend
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── services/
    │   └── hooks/
    └── public/
```

## API Documentation

Once running, visit `http://localhost:8000/docs` for interactive API documentation.

## License

MIT
" 
