# Docker Application

A full-stack web application built with React, Node.js, Express, and MongoDB, fully containerized using Docker and orchestrated with Docker Compose.

## 🎯 What We Wanted to Learn

This project was designed to master modern web development and containerization technologies:

- **Full-Stack Development**: Building a complete web application with separate frontend and backend
- **Docker Containerization**: Learning how to containerize applications for consistent deployment
- **Docker Compose**: Orchestrating multiple services and managing their dependencies
- **Microservices Architecture**: Understanding how to separate concerns between frontend, backend, and database
- **MongoDB Integration**: Working with NoSQL databases in a containerized environment
- **Production Deployment**: Deploying containerized applications to cloud platforms (Digital Ocean)
- **CI/CD Pipeline**: Implementing continuous integration and deployment workflows

## 🏗️ Architecture Overview

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   MongoDB       │
│   (React)       │◄──►│   (Node.js)     │◄──►│   Database      │
│   Port: 3000    │    │   Port: 5001    │    │   Port: 27017   │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 What We Have Built

### Frontend (React Application)
- **Technology**: React 19.1.1 with modern hooks
- **Features**:
  - Create new blog posts with title and content
  - View all existing posts in real-time
  - Responsive form handling
  - Clean, modern UI with inline styling
- **Containerization**: Multi-stage Docker build with Nginx for production serving

### Backend (Node.js API)
- **Technology**: Express.js 5.1.0 with MongoDB integration
- **Features**:
  - RESTful API endpoints for CRUD operations
  - MongoDB connection with Mongoose ODM
  - CORS enabled for cross-origin requests
  - Environment-based configuration
- **Endpoints**:
  - `GET /` - Health check endpoint
  - `GET /getPosts` - Retrieve all posts
  - `POST /posts` - Create new post

### Database (MongoDB)
- **Technology**: MongoDB 5 with persistent data storage
- **Features**:
  - Persistent data storage using Docker volumes
  - Network isolation for security
  - Automatic data persistence across container restarts

## 🐳 Docker Configuration

### Services Orchestration
- **MongoDB Service**: Database with persistent volume storage
- **Backend Service**: Node.js API server with MongoDB dependency
- **Frontend Service**: React application served via Nginx
- **Custom Network**: Isolated network for secure inter-service communication

### Container Images
- **Backend**: `sahilchalke1015/blog-backend:latest`
- **Frontend**: `sahilchalke1015/blog-frontend:latest`
- **Database**: `mongo:5` (official MongoDB image)

### Production Deployment
- **Platform**: Digital Ocean Droplet
- **Deployment**: Automated CI/CD pipeline
- **Status**: ✅ Live and accessible

## 🛠️ Technologies Used

### Frontend
- React 19.1.1
- React Hooks (useState, useEffect)
- Modern JavaScript (ES6+)
- Nginx (production web server)

### Backend
- Node.js 18
- Express.js 5.1.0
- Mongoose 8.18.1 (MongoDB ODM)
- CORS 2.8.5

### DevOps & Containerization
- Docker
- Docker Compose
- Multi-stage Docker builds
- Nginx reverse proxy
- Docker volumes for data persistence
- CI/CD Pipeline (GitHub Actions)
- Digital Ocean deployment

### Database
- MongoDB 5
- Mongoose ODM
- Persistent data storage

## 🎯 What We Have Achieved

### ✅ Technical Achievements
1. **Full-Stack Application**: Successfully built a complete web application with frontend, backend, and database
2. **Containerization Mastery**: Learned to containerize both frontend and backend applications
3. **Docker Compose Orchestration**: Mastered service orchestration and dependency management
4. **Production Deployment**: Successfully deployed to Digital Ocean with custom Docker images
5. **CI/CD Implementation**: Set up automated deployment pipeline for continuous integration and deployment
6. **Database Integration**: Implemented MongoDB with proper schema design and data persistence
7. **API Development**: Created RESTful APIs with proper error handling and CORS configuration

### ✅ Learning Outcomes
1. **Microservices Understanding**: Gained experience in building loosely coupled services
2. **Docker Best Practices**: Learned multi-stage builds, volume management, and network configuration
3. **Production Readiness**: Implemented production-grade containerization with Nginx
4. **Database Design**: Understood NoSQL database modeling with Mongoose
5. **Cloud Deployment**: Successfully deployed containerized applications to cloud platforms
6. **CI/CD Pipeline**: Mastered automated deployment workflows and continuous integration

### ✅ Project Highlights
- **Scalable Architecture**: Built with scalability and maintainability in mind
- **Production Ready**: Implemented proper containerization for production deployment
- **Live Deployment**: Successfully deployed on Digital Ocean with automated CI/CD
- **Modern Tech Stack**: Used latest versions of React, Node.js, and MongoDB
- **Clean Code**: Followed best practices for code organization and structure
- **Docker Expertise**: Mastered Docker and Docker Compose for container orchestration
- **DevOps Mastery**: Complete CI/CD pipeline implementation for automated deployments

## 🚀 Getting Started

### Prerequisites
- Docker
- Docker Compose

### Running the Application
```bash
# Clone the repository
git clone <repository-url>
cd docker-todo

# Start all services
docker-compose up -d

# View logs
docker-compose logs -f
```

### Access Points
- **Frontend**: http://localhost:3000
- **Backend API**: http://localhost:5001
- **MongoDB**: localhost:27017

### Production Access
- **Live Application**: Deployed on Digital Ocean Droplet
- **Automated Deployment**: CI/CD pipeline triggers on code changes
- **Status**: ✅ Production ready and accessible

## 📁 Project Structure
```
docker-todo/
├── frontend/                 # React application
│   ├── src/                 # Source code
│   ├── public/              # Static assets
│   ├── build/               # Production build
│   ├── Dockerfile           # Frontend container config
│   └── package.json         # Frontend dependencies
├── backend/                 # Node.js API
│   ├── server.js            # Main server file
│   ├── Dockerfile           # Backend container config
│   └── package.json         # Backend dependencies
├── docker-compose.yml       # Service orchestration
└── README.md               # This file
```

## 🔧 Development Workflow

1. **Local Development**: Each service can be run independently for development
2. **Container Development**: Use Docker Compose for integrated development
3. **Production Build**: Multi-stage Docker builds for optimized production images
4. **CI/CD Pipeline**: Automated testing, building, and deployment on code changes
5. **Cloud Deployment**: Push images to Docker Hub and deploy to Digital Ocean via CI/CD

## 🎉 Conclusion

This project successfully demonstrates mastery of modern full-stack development with containerization and DevOps. We've built a production-ready application that showcases:

- Complete understanding of React and Node.js development
- Proficiency in Docker containerization and orchestration
- Database design and integration skills
- Cloud deployment capabilities with Digital Ocean
- CI/CD pipeline implementation for automated deployments
- Modern development practices and best practices

The application is fully functional, containerized, deployed on Digital Ocean with automated CI/CD, and represents a significant achievement in full-stack development, DevOps practices, and production deployment automation.
