# Mergington High School Activities

A web application that allows students to browse extracurricular activities and enables teachers to manage student registrations at Mergington High School.

## Overview

This application consists of a FastAPI backend with a MongoDB database and a JavaScript-based frontend. Students can browse and search activities, while teachers can log in to register or unregister students for activities.

## Features

### For Students
- View all available extracurricular activities
- Browse activities by category (Sports, Arts, Academic, Community, Technology)
- Filter activities by day of the week (Monday through Sunday)
- Filter activities by time (Before School, After School, Weekend)
- Search for activities by name, description, or schedule
- See real-time activity capacity and availability
- View detailed activity information including schedule, description, and current participants

### For Teachers
- Secure login system with authentication
- Register students for activities
- Unregister students from activities
- All registration actions require teacher authentication

## Architecture

### Backend (Python/FastAPI)
- **Main Application**: `app.py` - FastAPI application setup and configuration
- **Database**: `backend/database.py` - MongoDB connection and initialization with sample data
- **API Routes**:
  - `backend/routers/activities.py` - Endpoints for viewing and managing activities
  - `backend/routers/auth.py` - Teacher authentication endpoints

### Frontend (HTML/CSS/JavaScript)
- **Main Page**: `static/index.html` - Single-page application structure
- **Styling**: `static/styles.css` - All visual styling and responsive design
- **Application Logic**: `static/app.js` - Activity display, filtering, search, and authentication

### Database (MongoDB)
- **Activities Collection**: Stores all extracurricular activities with schedules, participants, and capacity
- **Teachers Collection**: Stores teacher login credentials and display names

## API Endpoints

### Activities
- `GET /activities/` - Get all activities with optional filters (day, start_time, end_time)
- `GET /activities/days` - Get list of all days with scheduled activities
- `POST /activities/{activity_name}/signup` - Register a student for an activity (requires teacher authentication)
- `POST /activities/{activity_name}/unregister` - Remove a student from an activity (requires teacher authentication)

### Authentication
- `POST /auth/login` - Teacher login with username and password
- `GET /auth/check-session` - Verify teacher session validity

## Activity Categories

The system automatically categorizes activities into five types:
- **Sports**: Soccer Team, Basketball Team, Morning Fitness
- **Arts**: Art Club, Drama Club, Manga Maniacs
- **Academic**: Chess Club, Math Club, Debate Team, Science Olympiad
- **Technology**: Programming Class, Weekend Robotics Workshop
- **Community**: (Activities with volunteer or community service focus)

## Sample Teacher Accounts

The system includes three pre-configured teacher accounts:
- **Ms. Rodriguez** (username: mrodriguez) - Teacher role
- **Mr. Chen** (username: mchen) - Teacher role  
- **Principal Martinez** (username: principal) - Admin role

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
