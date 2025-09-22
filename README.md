# Node.js Demo App CI/CD with GitHub Actions + Docker

## 📌 Task Overview  
Automated the build and deployment of a Node.js application using **GitHub Actions** and **Docker**.  
The pipeline builds the app, creates a Docker image, pushes it to **DockerHub**, and allows deployment locally.  

---

## ⚙️ Steps Performed  

1. **Copied App Files**  
   - Used a simple Node.js app (`app.js`, `package.json`, `compile.json`).  

2. **Created Dockerfile**  
   - Added `Dockerfile` and `.dockerignore` for containerization.  

3. **Created GitHub Repository**  
   - Pushed the project files to a new GitHub repo.  

4. **Added GitHub Secrets**  
   - `DOCKER_USERNAME` → DockerHub username  
   - `DOCKER_PASSWORD` → DockerHub password/token  

5. **Created Workflow File**  
   - Added `.github/workflows/main.yml` with steps for:  
     - Checkout  
     - Install dependencies  
     - Test  
     - Build Docker image  
     - Push image to DockerHub  

6. **Pushed Code to GitHub**  
   - Triggered the GitHub Actions workflow.  
   - Workflow successfully built and pushed the image to DockerHub.  

7. **Deployment**  
   - Pulled the image from DockerHub locally.  
   - Ran the container with:  
     ```bash
     docker run -p 3000:3000 l4kshya/nodejs-demo-app:latest
     ```
   - Verified app at `http://localhost:3000`.

---

## ✅ Outcome  
- Automated CI/CD pipeline completed.  
- Docker image successfully available on DockerHub.  
- Application tested and deployed locally from the pushed image.  

