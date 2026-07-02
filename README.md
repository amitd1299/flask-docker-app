# flask-docker-app

## Multi-Environment CI/CD Pipeline | Jenkins | Docker | AWS EC2

### Project Overview
Automated CI/CD pipeline that automatically builds Docker images from GitHub commits and deploys to Dev, Staging, and Production environments with manual approval gates — simulating real-world progressive deployment practices.

### Tech Stack
- **Jenkins** — CI/CD Automation (Pipeline as Code)
- **Docker** — Containerization
- **AWS EC2** — Cloud Server (Ubuntu)
- **Flask (Python)** — Web Application
- **GitHub Webhooks** — Auto-trigger pipeline on every push

### Pipeline Flow
GitHub Push → Jenkins Auto-Trigger (Webhook) → Docker Image Build → Deploy to Dev (Auto) → Manual Approval → Deploy to Staging → Manual Approval → Deploy to Production

### Environments
| Environment | Port | Deployment |
|-------------|------|------------|
| Dev | 5000 | Automatic |
| Staging | 5001 | Manual Approval Required |
| Production | 5002 | Manual Approval Required |

### Key Features
- ✅ Pipeline as Code (Jenkinsfile in GitHub)
- ✅ Multi-environment deployment (Dev → Staging → Prod)
- ✅ Manual approval gates before Staging & Production
- ✅ GitHub Webhook — auto pipeline trigger on code push
- ✅ Docker containerization for consistent deployments

### Project Structure
flask-docker-app/
├── app.py              # Flask web application
├── Dockerfile          # Docker image configuration
├── Jenkinsfile         # CI/CD Pipeline definition
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation

### What I Learned
- Setting up Jenkins on AWS EC2 from scratch
- Writing declarative Jenkinsfile pipelines
- Docker image build and container management
- GitHub Webhook integration with Jenkins
- Multi-environment deployment strategy
- Manual approval gates in CI/CD pipelines
