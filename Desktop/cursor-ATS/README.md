# HATS - Hybrid Application Tracking System

A comprehensive MERN stack application for managing job applications with automated processing for technical roles and manual management for non-technical roles.

## 🚀 Features

### Role-Based Access Control
- **Applicant**: Submit applications, track status, view job listings
- **Admin**: Manage applications, create jobs, set keywords, manual shortlisting
- **Bot Mimic**: Automated processing of technical role applications

### Application Management
- **Detailed Application Forms**: Comprehensive 6-step application process
- **Resume Upload**: PDF, DOC, DOCX file support with validation
- **Keyword-Based Shortlisting**: Automated shortlisting for technical roles
- **Status Tracking**: Complete workflow from application to offer
- **Activity Logs**: Full audit trail of all application activities

### Responsive Design
- **Mobile-First**: Optimized for all screen sizes
- **Modern UI**: Clean, professional interface with excellent readability
- **Touch-Friendly**: Large buttons and optimized spacing for mobile devices

## 🛠️ Tech Stack

### Backend
- **Node.js** with Express.js
- **MongoDB** with Mongoose ODM
- **JWT** for authentication
- **Multer** for file uploads
- **bcryptjs** for password hashing

### Frontend
- **React** with functional components and hooks
- **React Router** for navigation
- **Axios** for API communication
- **Recharts** for data visualization
- **CSS3** with responsive design

## 📦 Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud)
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd cursor-ATS
   ```

2. **Install dependencies**
   ```bash
   npm run install-all
   ```

3. **Environment Setup**
   Create a `.env` file in the root directory:
   ```env
   MONGODB_URI=mongodb://localhost:27017/hats
   JWT_SECRET=your_jwt_secret_key
   PORT=5000
   ```

4. **Seed the database**
   ```bash
   npm run seed
   ```

5. **Start the application**
   ```bash
   npm run dev
   ```

## 🌐 Access URLs

- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5000

## 👥 Demo Credentials

| Role | Email | Password |
|------|-------|----------|
| Applicant | applicant@demo.com | password123 |
| Admin | admin@demo.com | password123 |
| Bot Mimic | bot@demo.com | password123 |

## 📱 Usage Guide

### For Applicants
1. **Login** with applicant credentials
2. **Browse Jobs** in the Jobs section
3. **Apply** by clicking "Apply Now" and filling the detailed form
4. **Track Status** in the Applications section
5. **View Details** of your applications and activity logs

### For Admins
1. **Login** with admin credentials
2. **Create Jobs** using the "Create New Job" button
3. **Set Keywords** for technical roles using the Keywords button
4. **Manage Applications** by viewing details and updating status
5. **Manual Shortlisting** for non-technical roles
6. **View Analytics** in the dashboard

### For Bot Mimic
1. **Login** with bot mimic credentials
2. **Process Applications** using the "Process Technical Applications" button
3. **View Results** of automated processing
4. **Monitor Dashboard** for system statistics

## 🔧 API Endpoints

### Authentication
- `POST /api/users/register` - User registration
- `POST /api/users/login` - User login
- `GET /api/users/me` - Get current user

### Jobs
- `GET /api/jobs` - Get all jobs
- `POST /api/jobs` - Create job (Admin only)
- `PUT /api/jobs/:id` - Update job (Admin only)
- `DELETE /api/jobs/:id` - Delete job (Admin only)

### Applications
- `GET /api/applications` - Get applications
- `POST /api/applications` - Submit application
- `PUT /api/applications/:id` - Update application status
- `GET /api/applications/:id/activity` - Get activity logs
- `GET /api/applications/:id/resume` - Download resume

### Bot Mimic
- `POST /api/bot-mimic/process` - Process technical applications
- `GET /api/bot-mimic/stats` - Get processing statistics

### Keywords
- `GET /api/keywords/:jobId` - Get keywords for job
- `POST /api/keywords` - Set keywords for job (Admin only)

### Dashboard
- `GET /api/dashboard` - Get dashboard statistics

## 📊 Database Schema

### Users
- `name`, `email`, `password`, `role` (applicant/admin/bot_mimic)

### Jobs
- `title`, `description`, `department`, `isTechnical`, `status`

### Applications
- `applicant`, `job`, `status`, `personalInfo`, `professionalInfo`
- `education`, `workExperience`, `skills`, `resume`, `coverLetter`
- `shortlistingInfo`, `notes`

### Keywords
- `job`, `keywords[]`, `minimumScore`, `isActive`

### ActivityLogs
- `application`, `action`, `fromStatus`, `toStatus`
- `performedBy`, `performedByRole`, `comment`, `isAutomated`

## 🚀 Deployment

### Local Development
```bash
npm run dev
```

### Production Build
```bash
npm run build
```

### Environment Variables for Production
```env
MONGODB_URI=your_production_mongodb_uri
JWT_SECRET=your_production_jwt_secret
NODE_ENV=production
PORT=5000
```

## 🧪 Testing

Run the API test suite:
```bash
node test-api.js
```

## 📝 Features Implemented

✅ **Role-Based Authentication & Dashboards**
✅ **Application Creation & Tracking**
✅ **Bot Mimic Login (Automated Updates)**
✅ **Admin Manual Updates**
✅ **Full Traceability with Activity Logs**
✅ **Resume Upload & Management**
✅ **Keyword-Based Shortlisting**
✅ **Responsive Mobile-First Design**
✅ **Modern UI with Professional Color Scheme**
✅ **Complete API Documentation**

## 🎯 Key Benefits

- **Automated Processing**: Reduces manual work for technical roles
- **Complete Transparency**: Full audit trail of all activities
- **Mobile Responsive**: Works seamlessly across all devices
- **Professional Design**: Clean, modern interface with excellent UX
- **Scalable Architecture**: Built with best practices for maintainability

## 📞 Support

For issues or questions, please check the documentation or create an issue in the repository.

---

**Built with ❤️ using the MERN Stack**