# mcbs
# MotionBook Studio

A modern, secure, AI-integrated audiobook & eBook selling platform built with React.js and Node.js.

## 🚀 Features

### Core Features
- **User Authentication**: Sign Up/Login with Email, Google, Facebook
- **Role-based Access**: Buyer and Admin roles
- **Secure File Protection**: No download capability, streaming only
- **Payment Integration**: SSLCOMMERZ, bKash, Nagad support
- **AI Recommendations**: Smart book suggestions
- **Admin Panel**: Complete content and user management

### Security Features
- ✅ Token-protected streaming
- ✅ Secure audio streaming only
- ✅ PDF.js viewer with download/print disabled
- ✅ Input validation (XSS, SQLi protected)
- ✅ Rate limiting and session control

### UI/UX Features
- 🎨 Sky Blue (#87CEEB) and Light Blue (#ADD8E6) theme
- 🎬 Motion graphic transitions
- 📱 Responsive design
- 🔤 Poppins & Inter fonts
- ✨ 3D styled modern UI

## 🏗️ Tech Stack

### Frontend
- **React.js** - UI Library
- **Tailwind CSS** - Styling
- **Framer Motion** - Animations
- **React Router** - Navigation
- **Heroicons** - Icons
- **PDF.js** - PDF viewing
- **React Player** - Audio/Video player

### Backend
- **Node.js + Express** - Server
- **MySQL** - Database
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **SSLCOMMERZ** - Payment gateway
- **Multer** - File uploads
- **Helmet** - Security

## 📋 Prerequisites

- Node.js (v16.4.2 or higher)
- MySQL Database
- SSLCOMMERZ Account (for payments)

## 🛠️ Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd MotionBook
   ```

2. **Install dependencies**
   ```bash
   # Install root dependencies
   npm install
   
   # Install all dependencies (frontend + backend)
   npm run install-all
   ```

3. **Database Setup**
   ```bash
   # Create MySQL database
   mysql -u root -p
   ```
   
   Then run the schema file:
   ```sql
   source backend/config/schema.sql
   ```

4. **Environment Configuration**
   
   Copy and configure the backend environment file:
   ```bash
   cd backend
   cp .env.example .env
   ```
   
   Update the `.env` file with your configurations:
   ```env
   # Database
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_mysql_password
   DB_NAME=motionbook_db
   
   # JWT
   JWT_SECRET=your_super_secret_jwt_key
   
   # SSLCOMMERZ
   SSLCOMMERZ_STORE_ID=your_store_id
   SSLCOMMERZ_STORE_PASSWORD=your_store_password
   ```

## 🚀 Running the Application

### Development Mode
```bash
# Run both frontend and backend concurrently
npm run dev

# Or run individually
npm run server  # Backend only (port 5000)
npm run client  # Frontend only (port 3000)
```

### Production Mode
```bash
# Backend
cd backend
npm start

# Frontend (build first)
cd frontend
npm run build
# Deploy the build folder to your hosting service
```

## 📂 Project Structure

```
MotionBook/
├── backend/
│   ├── config/          # Database configuration
│   ├── controllers/     # Route controllers
│   ├── middleware/      # Custom middleware
│   ├── models/          # Database models
│   ├── routes/          # API routes
│   ├── uploads/         # File uploads
│   ├── utils/           # Utility functions
│   └── server.js        # Main server file
├── frontend/
│   ├── public/          # Static assets
│   ├── src/
│   │   ├── components/  # React components
│   │   ├── pages/       # Page components
│   │   ├── utils/       # Utility functions
│   │   └── App.js       # Main App component
│   └── tailwind.config.js
└── package.json         # Root package.json
```

## 🔐 Default Admin Access

- **Email**: admin@motionbook.com
- **Password**: admin123

## 🎯 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile

### Books (Coming Soon)
- `GET /api/books` - Get all books
- `POST /api/books` - Create book (Admin)
- `GET /api/books/:id` - Get book details
- `PUT /api/books/:id` - Update book (Admin)
- `DELETE /api/books/:id` - Delete book (Admin)

## 🚧 Development Roadmap

### Phase 1: Core Platform ✅
- [x] Project setup
- [x] Database schema
- [x] User authentication
- [x] Modern UI design
- [ ] Book management system
- [ ] File upload system

### Phase 2: Advanced Features
- [ ] Payment integration (SSLCOMMERZ)
- [ ] Secure file streaming
- [ ] PDF.js integration
- [ ] Audio player with preview
- [ ] Admin dashboard

### Phase 3: AI & Enhancement
- [ ] AI recommendation system
- [ ] Advanced search & filters
- [ ] User activity tracking
- [ ] Email notifications
- [ ] Analytics dashboard

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support, email support@motionbook.com or create an issue in the repository.

---

**MotionBook Studio** - Experience the future of digital reading and listening! 📚🎧
