frontend-developer-task/
│
├── backend/
│   ├── src/
│   │   ├── config/        # DB connection
│   │   ├── middleware/    # Auth & error handlers
│   │   ├── models/        # Mongoose models
│   │   ├── routes/        # API routes
│   │   ├── utils/         # Validators, helpers
│   │   └── index.js       # App entry
│   ├── package.json
│   └── .env.example
│
└── frontend/
    ├── components/        # UI components
    ├── lib/               # API + auth utilities
    ├── pages/             # Next.js pages (login, signup, dashboard)
    ├── styles/
    ├── package.json
    └── .env.local


How to Run the Project Locally
1. Clone the repository
git clone <your-repo-url>
cd frontend-developer-task

🖥️ Backend Setup
Install dependencies
cd backend
npm install

Create .env file:
MONGO_URI=mongodb://127.0.0.1:27017/frontend_task
JWT_SECRET=your_secret_key
JWT_EXPIRES_IN=1d

Start backend
npm run dev


It should display:

MongoDB connected
Server running on 5000

🌐 Frontend Setup
Install dependencies
cd ../frontend
npm install

Create .env.local
NEXT_PUBLIC_API_URL=http://localhost:5000

Start frontend
npm run dev


Frontend runs at:

👉 http://localhost:3000

🧪 Testing the App
1. Signup a new user

Visit:
👉 http://localhost:3000/signup

2. Login

👉 http://localhost:3000/login

3. Dashboard Features

Create tasks

Edit tasks

Delete tasks

Search tasks

View profile

All actions communicate with the backend through authenticated routes.
