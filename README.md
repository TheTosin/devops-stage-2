# Full-Stack FastAPI and React Template

Welcome to the Full-Stack FastAPI and React template repository. This repository serves as a demo application for interns, showcasing how to set up and run a full-stack application with a FastAPI backend and a ReactJS frontend using ChakraUI.

## Project Structure

The repository is organized into two main directories:

- **frontend**: Contains the ReactJS application.
- **backend**: Contains the FastAPI application and PostgreSQL database integration.

Each directory has its own README file with detailed instructions specific to that part of the application.

## Getting Started

To get started with this template, please follow the instructions in the respective directories:

- [Frontend README](./frontend/README.md)
- [Backend README](./backend/README.md)
  
Ensure you have the following installed on your machine:

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

### Clone the Repository

```bash
git clone https://github.com/yourusername/repository url
cd fullstack-fastapi-react-template

###Environment Variables
Create a .env file in the root directory of the repository and add the necessary environment variables. Use the provided .env.example as a reference.

**Running the Application**
To start the application using Docker Compose, run the following command in the root directory:
docker-compose up --build

This command will build and start the Docker containers for both the frontend and backend services.

**Access the Application**
Frontend: http://localhost:3000
Backend: http://localhost:8000

**Frontend**
The frontend is built with ReactJS and ChakraUI.

**Development**
To start the frontend in development mode, navigate to the frontend directory and run:
cd frontend
npm install
npm start

This will start the React development server on http://localhost:3000.

**Production**
The frontend production build is automatically created and served via Docker Compose. To create a production build manually, run:
npm run build

**Backend**
The backend is built with FastAPI and integrates with a PostgreSQL database.

**Development**
To start the backend in development mode, navigate to the backend directory and run:
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload

This will start the FastAPI server on http://localhost:8000.

**Database Migrations**
To handle database migrations, we use Alembic. Navigate to the backend directory and run:
alembic upgrade head

**Contributing**
We welcome contributions from the community. If you have suggestions for improvements, feel free to create a pull request or open an issue.

**License**
This project is licensed under the MIT License. See the LICENSE file for details.
For more detailed instructions, refer to the README files in the frontend and backend directories.




