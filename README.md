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

## ScreenShots

<img width="479" height="289" alt="local run capture" src="https://github.com/user-attachments/assets/cbd40a08-bb96-4ad4-82d4-6886d18f6f3e" />

---

<img width="707" height="312" alt="server running" src="https://github.com/user-attachments/assets/c69fa5ea-cc8e-441e-b391-3c7143fd14d4" />


## ✅ Outcome  
- Automated CI/CD pipeline completed.  
- Docker image successfully available on DockerHub.  
- Application tested and deployed locally from the pushed image.  

