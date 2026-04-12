# Government Services Assistant 🏛️

AI-powered multilingual platform for Indian government services - Hackathon MVP

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ 
- npm or yarn
- AWS Account (for deployment)

### Local Development

1. **Clone and install dependencies**
```bash
npm install
cd backend && npm install
cd ../frontend && npm install
```

2. **Setup environment variables**
```bash
cd backend
cp .env.example .env
# Edit .env with your configuration
```

3. **Run the application locally**
```bash
# From root directory
npm run dev
```

Backend will run on `http://localhost:5000`
Frontend will run on `http://localhost:5173`

### Deployment (AWS)

**Frontend Deployment (AWS Amplify):**
```bash
# Install Amplify CLI
npm install -g @aws-amplify/cli

# Initialize and deploy
cd frontend
amplify init
amplify add hosting
amplify publish
```

**Backend Deployment (AWS Elastic Beanstalk):**
```bash
# Install EB CLI
pip install awsebcli

# Initialize and deploy
cd backend
eb init
eb create
eb deploy
```

## 📁 Project Structure

```
gov-services-assistant/
├── backend/                 # Node.js + Express + TypeScript
│   ├── src/
│   │   ├── controllers/    # Request handlers
│   │   ├── routes/         # API routes
│   │   ├── middleware/     # Auth, validation
│   │   └── index.ts        # Entry point
│   └── package.json
├── frontend/               # React + TypeScript (to be created)
└── .kiro/specs/           # Project documentation
```

## 🛠️ Tech Stack

### Backend
- **Runtime**: Node.js + TypeScript
- **Framework**: Express.js
- **Deployment**: AWS Elastic Beanstalk
- **Database**: Amazon RDS (PostgreSQL) - planned
- **Cache**: Amazon ElastiCache (Redis) - planned
- **Auth**: JWT + bcrypt

### Frontend
- **Framework**: React 18 + TypeScript
- **Deployment**: AWS Amplify
- **CDN**: Amazon CloudFront
- **UI Library**: Material-UI
- **State**: Redux Toolkit

### AI/ML (AWS)
- **Amazon Bedrock**: AI recommendations (planned)
- **Amazon Translate**: Multilingual support (planned)
- **Amazon Personalize**: ML-based recommendations (planned)

## 📋 API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/verify-otp` - Verify OTP
- `POST /api/auth/logout` - Logout user

### Schemes
- `GET /api/schemes` - Get all schemes
- `GET /api/schemes/:id` - Get scheme by ID
- `GET /api/schemes/search` - Search schemes
- `GET /api/schemes/recommended/me` - Get personalized recommendations
- `POST /api/schemes/:id/check-eligibility` - Check eligibility

### User
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update profile
- `GET /api/users/applications` - Get user applications

## 🎯 Current Status

✅ Backend API structure
✅ Authentication routes
✅ Scheme management
✅ Mock data for demo (15 real government schemes)
✅ Frontend React app with Material-UI
⏳ AWS deployment (Amplify + Elastic Beanstalk)
⏳ Database integration (Amazon RDS)
⏳ AI integration (Amazon Bedrock, Amazon Translate)

## 💰 Cost Estimate

**Monthly Cost**: ₹300-450
- Amazon Bedrock (AI): ₹200-300 (planned)
- Amazon Translate: ₹100-150 (planned)
- AWS Free Tier: ₹0 (Amplify, Elastic Beanstalk, S3, CloudFront)

**Note**: MVP uses mock data and free tier services. AI services will be integrated in production.

## 🤝 Contributing

This is a hackathon project. Feel free to contribute!

## 📄 License

MIT
