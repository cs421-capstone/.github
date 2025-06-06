# CS 421 Capstone Project

## Overview
This GitHub organization contains the repositories for the CS 421 Capstone Project, which aims to design, build, and deploy a mini-Netumo service. This service will monitor target URLs, check SSL certificates and domain expiry, and send alerts via email and webhooks. The project is divided into several components, each with its own repository.

## Project Structure
The project is divided into the following repositories:

1. **Frontend**:
   - **Description**: Vue.js dashboard for monitoring target URLs with color-coded status, latency, SSL/domain countdown, and 24-hour uptime chart.
   - **Repository**: [frontend](https://github.com/cs421-capstone/frontend)
   - **Documentation**: [README](https://github.com/cs421-capstone/frontend/blob/main/README.md)

2. **API**:
   - **Description**: Spring Boot API with JWT-secured CRUD endpoints for managing monitoring targets, status, history, and alerts.
   - **Repository**: [api](https://github.com/cs421-capstone/api)
   - **Documentation**: [README](https://github.com/cs421-capstone/api/blob/main/README.md)

3. **Worker**:
   - **Description**: Celery worker with Redis for asynchronous monitoring tasks, including HTTP/HTTPS requests, SSL validity, and domain expiry checks.
   - **Repository**: [worker](https://github.com/cs421-capstone/worker)
   - **Documentation**: [README](https://github.com/cs421-capstone/worker/blob/main/README.md)

4. **Database**:
   - **Description**: PostgreSQL database schema and setup for storing monitoring targets, status, history, and alerts with connection pooling and daily backups.
   - **Repository**: [database](https://github.com/cs421-capstone/database)
   - **Documentation**: [README](https://github.com/cs421-capstone/database/blob/main/README.md)

5. **CI/CD**:
   - **Description**: CI/CD pipeline using GitHub Actions for linting, testing, building Docker images, pushing to Docker Hub, and deploying to AWS EC2.
   - **Repository**: [ci-cd](https://github.com/cs421-capstone/ci-cd)
   - **Documentation**: [README](https://github.com/cs421-capstone/ci-cd/blob/main/README.md)

## Getting Started
To get started with the project, follow these steps:

1. **Clone the Repositories**:
   - Frontend: `git clone https://github.com/cs421-capstone/frontend.git`
   - API: `git clone https://github.com/cs421-capstone/api.git`
   - Worker: `git clone https://github.com/cs421-capstone/worker.git`
   - Database: `git clone https://github.com/cs421-capstone/database.git`
   - CI/CD: `git clone https://github.com/cs421-capstone/ci-cd.git`

2. **Install Dependencies**:
   - Frontend: `npm install`
   - API: `mvn clean install`
   - Worker: `pip install -r requirements.txt`
   - Database: `docker build -t database .`

3. **Run the Services**:
   - Frontend: `npm run serve`
   - API: `mvn spring-boot:run`
   - Worker: `celery -A worker worker --loglevel=info`
   - Database: `docker run -d -p 5432:5432 database`

4. **Set Up CI/CD**:
   - Configure GitHub Actions workflows in the `ci-cd` repository.
   - Push changes to trigger the CI/CD pipeline.

## Contributing
To contribute to the project, follow these guidelines:

1. **Fork the Repository**: Fork the repository you want to contribute to.
2. **Create a Branch**: Create a new branch for your feature or fix.
3. **Make Changes**: Make your changes and commit them.
4. **Push Changes**: Push your changes to your fork.
5. **Create a Pull Request**: Create a pull request from your fork to the main repository.

## Team
- **Dr. Goodiel C. Moshi**: Instructor
- **Team Members**: [List all team members here]

## Contact
For any questions or issues, please contact the instructor at [goodiel.moshi@udom.ac.tz](mailto:goodiel.moshi@udom.ac.tz).

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [GitHub](https://github.com/)
- [AWS](https://aws.amazon.com/)
- [Docker](https://docker.com/)
- [Vue.js](https://vuejs.org/)
- [Spring Boot](https://spring.io/projects/spring-boot)
- [Celery](https://celeryproject.org/)
- [PostgreSQL](https://www.postgresql.org/)
