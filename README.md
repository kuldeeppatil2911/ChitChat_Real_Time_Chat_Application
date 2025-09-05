# ChitChat - Real-Time Chat Application

A modern, full-stack real-time chat application built with React, Node.js, and Socket.IO.

## Features

- **Real-time messaging** with Socket.IO
- **User authentication** with JWT
- **File/image sharing** with Cloudinary integration
- **Responsive design** with Tailwind CSS and DaisyUI
- **Modern UI** with Lucide React icons
- **State management** with Zustand
- **Hot toast notifications**

## Tech Stack

### Frontend
- React 18
- Vite
- Tailwind CSS + DaisyUI
- Socket.IO Client
- Zustand (State Management)
- React Router DOM
- Axios
- React Hot Toast

### Backend
- Node.js + Express
- Socket.IO
- MongoDB + Mongoose
- JWT Authentication
- Bcrypt.js
- Cloudinary
- CORS

## Prerequisites

- Node.js (v16 or higher)
- MongoDB
- Cloudinary account (for image uploads)

## Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd REAL-TIME-CHAT-APPLICATION(ChitChat)
   ```

2. **Install dependencies**
   ```bash
   npm run build
   ```

3. **Environment Setup**
   
   Create a `.env` file in the `backend` directory:
   ```env
   PORT=5001
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   NODE_ENV=development
   ```

## Running the Application

### Development Mode

1. **Start the backend server**
   ```bash
   cd backend
   npm run dev
   ```

2. **Start the frontend development server**
   ```bash
   cd frontend
   npm run dev
   ```

3. **Access the application**
   - Frontend: http://localhost:5173
   - Backend API: http://localhost:5001

### Production Mode

```bash
npm start
```

## Project Structure

```
REAL-TIME-CHAT-APPLICATION(ChitChat)/
├── backend/
│   ├── src/
│   │   ├── controllers/     # Route controllers
│   │   ├── lib/            # Database and socket configuration
│   │   ├── middleware/     # Authentication middleware
│   │   ├── models/         # MongoDB models
│   │   ├── routes/         # API routes
│   │   ├── seeds/          # Database seeders
│   │   └── index.js        # Server entry point
│   └── package.json
├── frontend/
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── constants/      # App constants
│   │   ├── lib/           # Utilities and configurations
│   │   ├── pages/         # Page components
│   │   ├── store/         # Zustand store
│   │   └── App.jsx        # Main App component
│   └── package.json
└── package.json           # Root package.json
```

## API Endpoints

### Authentication
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/check` - Check authentication status

### Messages
- `GET /api/messages/users` - Get all users
- `GET /api/messages/:id` - Get messages with specific user
- `POST /api/messages/send/:id` - Send message to user

## Socket Events

- `connection` - User connects
- `disconnect` - User disconnects
- `newMessage` - Send/receive new message
- `getOnlineUsers` - Get list of online users

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.