# CourseMaster - Frontend
Live Link: https://course-master4981.netlify.app/

Video link: https://drive.google.com/file/d/1vjMrBxr0-7xqjxMX2EBEBw30D_av1pOu/view

A modern E-learning platform frontend built with React, Redux Toolkit, and Tailwind CSS.

## Project Name & Description

**CourseMaster** is an E-learning platform where students can browse, enroll in, and consume courses. The frontend provides an interface for students to watch video lectures, complete assignments, and take quizzes. Administrators can manage courses and users, track enrollments, review assignments, and view analytics through a dedicated admin dashboard.

This is the frontend application of the CourseMaster platform, built with modern React technologies and responsive design principles.

## Technology Stack

- **React 19** - UI library
- **Vite** - Build tool and dev server
- **Redux Toolkit** - State management
- **React Router DOM** - Routing
- **Tailwind CSS + DaisyUI** - Styling
- **Axios** - HTTP client

## Installation

1. Clone the repository
2. Navigate to the repository root:
   ```bash
   cd courseMaster_Frontend
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

4. Optionally create a `.env` file in the root directory. The checked-in `.env.example` uses the deployed backend URL. For local development, set `VITE_API_BASE_URL` to your local backend URL.

5. Start the development server:
   ```bash
   npm run dev
   ```

6. Build for production:
   ```bash
   npm run build
   ```

## Environment Variables

The frontend reads the backend base URL from `VITE_API_BASE_URL`. The checked-in `.env.example` points to the deployed backend; copy it to `.env` if you want to use that URL, or set the variable to your own backend:

```env
# Example: local backend
VITE_API_BASE_URL=http://localhost:5000/api
```

If the variable is omitted, the frontend defaults to `http://localhost:5000/api`.

## Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── CourseCard/     # Course listing components
│   └── shared/         # Shared components (Navbar, Footer, Logo)
├── layouts/            # Layout components
├── pages/              # Page components
│   ├── admin/          # Admin dashboard pages
│   ├── CoursePlayer/   # Course video player
│   ├── CousrseDetails/ # Course details page
│   ├── Home/           # Home page with course listing
│   ├── Login/          # Login page
│   ├── Register/       # Registration page
│   └── student/        # Student dashboard
├── routes/              # Route protection components
├── services/           # API service functions
├── store/              # Redux store and slices
└── utils/              # Utility functions
```

## Features

### Public Features
- Browse courses with pagination, search, sorting, and filtering
- View detailed course information
- User registration and login

### Student Features
- Enroll in courses
- Watch video lectures (YouTube integration)
- Mark lessons as complete
- Track learning progress
- Submit assignments (text or Google Drive links)
- Take quizzes with immediate score feedback
- View enrolled courses dashboard

### Admin Features
- Create, update, and delete courses
- Add course syllabus (modules, lessons, videos, assignments, quizzes)
- Manage course batches
- View all enrollments
- Review and grade student assignments
- Filter enrollments by course/student
- Filter assignments by status
- Manage users, including changing roles, banning/unbanning, and deleting accounts
- Manage video classes

## API Integration

The frontend communicates with the backend API. All API endpoints are documented in the backend README.

The frontend uses these API areas:

- **Authentication**: `/auth/register`, `/auth/login`, `/auth/me`
- **Courses**: `/courses` (list and details)
- **Enrollments**: `/enrollments` (enroll, list the current user's enrollments, and mark lessons complete)
- **Assignments and quizzes**: submit work and retrieve the current user's submissions and stats
- **Admin**: course, enrollment, assignment review, analytics, and user-management endpoints

For complete API documentation with request/response formats, see [courseMaster_Backend/README.md](../courseMaster_Backend/README.md).

Admin access is determined by the account role provided by the backend. Use an authorized admin account; this repository does not provide shared admin credentials.

## Development

- Development server runs on `http://localhost:5173` (default Vite port)
- Hot Module Replacement (HMR) is enabled
- Run `npm run lint` to check code quality
- Run `npm run build` to create a production build

## Deployment

The frontend can be deployed to:
- **Netlify**
