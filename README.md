# PaintFlow.ai

PaintFlow.ai is a supply chain intelligence platform designed for paint manufacturing and distribution. It combines forecasting, inventory analysis, AI-powered recommendations, and operational analytics into a single system for admins, dealers, and customers.

The platform includes:

- Admin Portal for supply chain monitoring and analytics
- Dealer Portal for inventory and order management
- Customer Portal for paint discovery and shade matching

---

## Tech Stack

| Category | Technologies |
|----------|--------------|
| Frontend | React 19, Vite, TailwindCSS 4, Recharts |
| Backend | FastAPI, Python 3.10+, SQLAlchemy |
| Database | SQLite |
| ML Models | Prophet |
| AI Integration | Google Gemini 1.5 Flash |
| Maps | react-simple-maps |

---

## Main Features

### Demand Forecasting
Forecast future product demand using Prophet-based time series models with seasonal trend analysis.

### Inventory Optimization
Track stock levels, identify dead stock, and monitor stockout risks across warehouses.

### Smart Order Recommendations
Generate dealer-side order suggestions based on inventory movement and demand trends.

### AI Copilot
Conversational assistant powered by Gemini for operational queries and analytics insights.

### Scenario Simulation
Run supply chain simulations for events like:
- Truck strikes
- Heatwaves
- Early monsoons

### Snap & Find
Match paint shades from uploaded images or HEX color values.

### Warehouse Network Map
Visualize warehouse locations and inventory transfer routes across India.

---

# Local Setup

## 1. Clone Repository

```bash
git clone https://github.com/Arijit2772-dev/hacktu7.0.git
cd hacktu7.0
```

---

## 2. Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv
```

### Activate Environment

#### Windows

```bash
venv\Scripts\activate
```

#### macOS / Linux

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Configure Gemini API Key (Optional)

#### Windows

```bash
set GEMINI_API_KEY=your_api_key
```

#### macOS / Linux

```bash
export GEMINI_API_KEY="your_api_key"
```

### Seed Database and Train Models

```bash
python seed_and_train.py
```

### Start Backend Server

```bash
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

Backend available at:

```bash
http://localhost:8000
```

Swagger Docs:

```bash
http://localhost:8000/docs
```

---

## 3. Frontend Setup

Open a new terminal window.

```bash
cd frontend

npm install
npm run dev
```

Frontend available at:

```bash
http://localhost:5173
```

---

## Portal Overview

| Portal | Description |
|--------|-------------|
| Admin | Forecasting, inventory tracking, analytics |
| Dealer | Smart orders, order tracking, dealer insights |
| Customer | Shade catalog, dealer finder, color matcher |

---

## Project Structure

```bash
hacktu7.0/
│
├── backend/
│   ├── app/
│   ├── seed/
│   ├── requirements.txt
│   └── seed_and_train.py
│
├── frontend/
│   ├── src/
│   ├── vite.config.js
│   └── package.json
│
└── README.md
```

---

## Environment Variables

| Variable | Required | Description |
|----------|----------|-------------|
| GEMINI_API_KEY | No | Gemini API key for AI copilot |

---

## API Documentation

| Docs | URL |
|------|-----|
| Swagger UI | `http://localhost:8000/docs` |
| ReDoc | `http://localhost:8000/redoc` |

---

## Build for Production

```bash
cd frontend
npm run build
```

Production build files will be generated in:

```bash
frontend/dist/
```

---

## License

MIT License
