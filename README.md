# MERN Stack Docker Application

A full-stack application template using MongoDB, Express.js, React.js, and Node.js (MERN), all containerized with Docker.

## 🚀 Features

- **Docker** containerization for consistent development and production environments
- **React** frontend with hot-reload
- **Node.js** and **Express** backend
- **MongoDB** database with persistent storage
- Development and production configurations
- Docker Compose orchestration
- Environment variable management

## 📋 Prerequisites

Make sure you have the following installed:
- Docker (20.10.x or higher)
- Docker Compose (2.x.x or higher)
- Git

## 🛠️ Project Structure

```
project-root/
├── docker-compose.yml
├── .gitignore
├── README.md
├── frontend/
│   ├── Dockerfile
│   ├── package.json
│   └── src/
├── backend/
│   ├── Dockerfile
│   ├── package.json
│   └── src/
```

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone git@github.com:gitsaket/simple-MERN-Docker-compose-setup.git 
cd simple-MERN-Docker-compose-setup
```

### 2. Environment Setup

Create `.env` files in both frontend and backend directories:

Frontend `.env`:
```env
REACT_APP_API_URL=http://localhost:5000
```

Backend `.env`:
```env
PORT=5000
MONGODB_URI=mongodb://mongodb:27017/myapp
```

### 3. Start the Application

```bash
# Build and start all containers
docker-compose up --build

# Run in detached mode (optional)
docker-compose up -d --build
```

The application will be available at:
- Frontend: http://localhost:3000
- Backend API: http://localhost:5000
- MongoDB: localhost:27017

## 🔧 Development

### Running Individual Services

```bash
# Start specific service
docker-compose up frontend
docker-compose up backend
docker-compose up mongodb

# Rebuild specific service
docker-compose up --build frontend
```

### Viewing Logs

```bash
# View all logs
docker-compose logs

# View specific service logs
docker-compose logs frontend
docker-compose logs backend
```

### Stopping the Application

```bash
# Stop all containers
docker-compose down

# Stop and remove volumes (careful - this will delete MongoDB data)
docker-compose down -v
```

## 📦 Available Scripts

Frontend:
```bash
npm start    # Start development server
npm test     # Run tests
npm build    # Create production build
```

Backend:
```bash
npm start    # Start server
npm run dev  # Start server with nodemon
npm test     # Run tests
```

## 🔑 Environment Variables

### Frontend
| Variable | Description | Default |
|----------|-------------|---------|
| REACT_APP_API_URL | Backend API URL | http://localhost:5000 |

### Backend
| Variable | Description | Default |
|----------|-------------|---------|
| PORT | Server port | 5000 |
| MONGODB_URI | MongoDB connection string | mongodb://mongodb:27017/myapp |

## 📚 Additional Documentation

- [Frontend Documentation](./frontend/README.md)
- [Backend Documentation](./backend/README.md)
- [API Documentation](./backend/API.md)

## 🛡️ Security

- All sensitive information is stored in environment variables
- MongoDB is not exposed to the public by default
- CORS is configured for security
- Dependencies are regularly updated

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Docker Documentation](https://docs.docker.com/)
- [React Documentation](https://reactjs.org/)
- [Express Documentation](https://expressjs.com/)
- [MongoDB Documentation](https://docs.mongodb.com/)

## 📧 Contact

Your Name - [your.email@example.com](mailto:your.email@example.com)

Project Link: [https://github.com/yourusername/project-name](https://github.com/yourusername/project-name)
