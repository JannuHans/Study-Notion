# 🎓 LearnEdge - EdTech Platform

A full-stack educational technology platform built with the MERN stack, enabling instructors to create and sell courses while providing students with a seamless learning experience.

![MERN Stack](https://img.shields.io/badge/Stack-MERN-green)
![React](https://img.shields.io/badge/React-18.2.0-blue)
![Node.js](https://img.shields.io/badge/Node.js-16.18.0-green)
![MongoDB](https://img.shields.io/badge/MongoDB-7.0-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 📋 Table of Contents

- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Demo](#-demo)
- [Screenshots](#-screenshots)
- [Installation](#-installation)
- [Environment Variables](#-environment-variables)
- [Usage](#-usage)
- [API Documentation](#-api-documentation)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## ✨ Features

### For Students
- 🔐 Secure user authentication with JWT
- 📚 Browse and search courses by category
- 🛒 Shopping cart functionality
- 💳 Secure payment processing via Razorpay
- 📹 Watch video lectures with progress tracking
- ⭐ Rate and review courses
- 📊 Track learning progress
- 📧 Email notifications for enrollment and updates

### For Instructors
- 📝 Create and manage courses
- 🎬 Upload video lectures and course materials
- 💰 Set course pricing
- 📈 View analytics and earnings
- 👥 Track student enrollments
- ✏️ Edit and update course content
- 📊 Instructor dashboard with statistics

### For Admins
- 🏷️ Create and manage course categories
- 👤 User management
- 📊 Platform analytics
- 🔧 System configuration

---

## 🛠️ Tech Stack

### Frontend
- **React 18.2.0** - UI library
- **Redux Toolkit** - State management
- **React Router DOM** - Client-side routing
- **Tailwind CSS** - Styling framework
- **Axios** - HTTP client
- **React Hook Form** - Form handling
- **React Hot Toast** - Notifications
- **Chart.js** - Data visualization
- **Video React** - Video player
- **Swiper** - Touch slider

### Backend
- **Node.js** - JavaScript runtime
- **Express.js** - Web framework
- **MongoDB** - NoSQL database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **Bcrypt** - Password hashing
- **Nodemailer** - Email service
- **Cloudinary** - Media storage
- **Razorpay** - Payment gateway

### Development Tools
- **Nodemon** - Auto-restart server
- **Concurrently** - Run multiple commands
- **Prettier** - Code formatter

---

## 🎬 Demo

🔗 **Live Demo**: https://courageous-shortbread-7b78e0.netlify.app/

### Test Credentials
```
Student Account:
Email: student@example.com
Password: student123

Instructor Account:
Email: instructor@example.com
Password: instructor123
```

---

## 📸 Screenshots

### Home Page
![Home Page](screenshots/home.png)

### Course Catalog
![Course Catalog](screenshots/catalog.png)

### Course Details
![Course Details](screenshots/course-details.png)

### Student Dashboard
![Student Dashboard](screenshots/student-dashboard.png)

### Instructor Dashboard
![Instructor Dashboard](screenshots/instructor-dashboard.png)

---

## 🚀 Installation

### Prerequisites
- Node.js (v16.18.0 or higher)
- MongoDB (local or Atlas)
- npm or yarn
- Git

### Clone Repository
```bash
git clone https://github.com/YOUR-USERNAME/learnedge.git
cd learnedge
```

### Install Dependencies

**Frontend:**
```bash
npm install
```

**Backend:**
```bash
cd server
npm install
```

### Setup Environment Variables

Create `.env` file in root directory:
```env
REACT_APP_BASE_URL=http://localhost:4000/api/v1
```

Create `server/.env` file:
```env
PORT=4000
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUD_NAME=your_cloudinary_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
RAZORPAY_KEY=your_razorpay_key
RAZORPAY_SECRET=your_razorpay_secret
MAIL_HOST=smtp.gmail.com
MAIL_USER=your_email@gmail.com
MAIL_PASS=your_app_password
FRONTEND_URL=http://localhost:3000
SUPPORT_EMAIL=support@example.com
```

### Run Application

**Development Mode (Both Frontend & Backend):**
```bash
npm run dev
```

**Or Run Separately:**

Frontend:
```bash
npm start
```

Backend:
```bash
cd server
npm run dev
```

### Access Application
- Frontend: https://courageous-shortbread-7b78e0.netlify.app/
- Backend: https://learnedge-backend-rn1w.onrender.com

---

## 🔐 Environment Variables

### Frontend Variables
| Variable | Description | Example |
|----------|-------------|---------|
| `REACT_APP_BASE_URL` | Backend API URL | `http://localhost:4000/api/v1` |

### Backend Variables
| Variable | Description | Required |
|----------|-------------|----------|
| `PORT` | Server port | No (default: 4000) |
| `MONGODB_URL` | MongoDB connection string | Yes |
| `JWT_SECRET` | JWT signing secret | Yes |
| `CLOUD_NAME` | Cloudinary cloud name | Yes |
| `API_KEY` | Cloudinary API key | Yes |
| `API_SECRET` | Cloudinary API secret | Yes |
| `RAZORPAY_KEY` | Razorpay key ID | Yes |
| `RAZORPAY_SECRET` | Razorpay secret | Yes |
| `MAIL_HOST` | SMTP host | Yes |
| `MAIL_USER` | Email address | Yes |
| `MAIL_PASS` | Email password | Yes |
| `FRONTEND_URL` | Frontend URL | Yes |
| `SUPPORT_EMAIL` | Support email | Yes |

---

## 💻 Usage

### For Students

1. **Sign Up**: Create a student account
2. **Browse Courses**: Explore available courses by category
3. **Add to Cart**: Select courses you want to purchase
4. **Checkout**: Complete payment via Razorpay
5. **Learn**: Access enrolled courses and watch lectures
6. **Track Progress**: Monitor your learning progress
7. **Rate & Review**: Share your feedback on courses

### For Instructors

1. **Sign Up**: Create an instructor account
2. **Create Course**: Add course details, sections, and lectures
3. **Upload Content**: Upload videos and course materials
4. **Set Pricing**: Define course price
5. **Publish**: Make course available to students
6. **Monitor**: Track enrollments and earnings
7. **Update**: Edit course content anytime

---

## 📚 API Documentation

### Base URL
```
Development: http://localhost:4000/api/v1
Production: YOUR_DEPLOYED_URL/api/v1
```

### Authentication Endpoints

#### Register User
```http
POST /auth/signup
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "password": "password123",
  "confirmPassword": "password123",
  "accountType": "Student",
  "otp": "123456"
}
```

#### Login
```http
POST /auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "password123"
}
```

### Course Endpoints

#### Get All Courses
```http
GET /course/getAllCourses
```

#### Get Course Details
```http
POST /course/getCourseDetails
Content-Type: application/json

{
  "courseId": "course_id_here"
}
```

#### Create Course (Instructor Only)
```http
POST /course/createCourse
Authorization: Bearer <token>
Content-Type: multipart/form-data

{
  "courseName": "Course Name",
  "courseDescription": "Description",
  "price": 999,
  "category": "category_id",
  "thumbnailImage": <file>
}
```

### Payment Endpoints

#### Capture Payment
```http
POST /payment/capturePayment
Authorization: Bearer <token>
Content-Type: application/json

{
  "courses": ["course_id_1", "course_id_2"]
}
```

---

## 📁 Project Structure

```
learnedge/
├── public/                 # Static files
├── src/                    # Frontend source code
│   ├── assets/            # Images, logos, videos
│   ├── components/        # React components
│   │   ├── Common/       # Shared components
│   │   └── core/         # Feature-specific components
│   ├── data/             # Static data
│   ├── hooks/            # Custom React hooks
│   ├── pages/            # Page components
│   ├── services/         # API services
│   ├── slices/           # Redux slices
│   ├── utils/            # Utility functions
│   ├── App.jsx           # Main app component
│   └── index.js          # Entry point
├── server/                # Backend source code
│   ├── config/           # Configuration files
│   ├── controllers/      # Request handlers
│   ├── mail/             # Email templates
│   ├── middleware/       # Custom middleware
│   ├── models/           # Database models
│   ├── routes/           # API routes
│   ├── utils/            # Utility functions
│   └── index.js          # Server entry point
├── .env.example          # Environment variables template
├── package.json          # Dependencies
└── README.md            # This file
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Make your changes
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
5. Push to the branch (`git push origin feature/AmazingFeature`)
6. Open a Pull Request

### Coding Standards
- Follow existing code style
- Write meaningful commit messages
- Add comments for complex logic
- Update documentation as needed

---

## 🧪 Testing

```bash
# Run frontend tests
npm test

# Run backend tests
cd server
npm test
```

---

## 🚀 Deployment

### Frontend (Netlify)
1. Build the project: `npm run build`
2. Deploy the `build/` folder to Netlify
3. Set environment variables in Netlify dashboard

### Backend (Render)
1. Push code to GitHub
2. Connect repository to Render
3. Set environment variables
4. Deploy

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Akhilesh Pratap Singh**

- GitHub: [@Akhilesh Pratap Singh](https://github.com/your-username)
- LinkedIn: [Akhilesh Pratap Singh](https://linkedin.com/in/your-profile)
- Email: your.email@example.com
- Portfolio: [your-portfolio.com](https://your-portfolio.com)

---

## 🙏 Acknowledgments

- [React Documentation](https://react.dev/)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/)
- [Tailwind CSS](https://tailwindcss.com/)
- [Cloudinary](https://cloudinary.com/)
- [Razorpay](https://razorpay.com/)

---

## 📞 Support

For support, email support@example.com or join our Slack channel.

---

## 🔮 Future Enhancements

- [ ] Live classes feature
- [ ] Discussion forums
- [ ] Assignments and quizzes
- [ ] Certificates upon completion
- [ ] Mobile application
- [ ] AI-powered course recommendations
- [ ] Multi-language support
- [ ] Offline mode
- [ ] Social learning features

---

## 📊 Project Status

🟢 **Active Development** - This project is actively maintained and updated regularly.

---

## ⭐ Show Your Support

Give a ⭐️ if you like this project!

---

<div align="center">
  <p>Made with ❤️ by Akhilesh Pratap Singh</p>
  <p>© 2025 LearnEdge. All rights reserved.</p>
</div>

