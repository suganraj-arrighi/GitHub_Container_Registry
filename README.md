# 📦 GitHub Container Registry - GHCR Demo

This is a simple Node.js application containerized with Docker and published to **GitHub Container Registry (GHCR)**.  
Ideal for beginners exploring Docker, GitHub Actions, and DevOps workflows.

---

## 🚀 How to Use

### 🔧 Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Git](https://git-scm.com/)
- A GitHub account with a [Personal Access Token (PAT)](https://github.com/settings/tokens)

---

### 📁 Create Project Folder and Initialize Git

```bash
mkdir github-container-registr
cd github-container-registr
git init
```
### Create a sample JS file on whatever the code you want to build as a registry

## How to push and pull 

### 🐳 Build the Docker Image

```bask
docker build -t ghcr.io/YOUR_GITHUB_USERNAME/github_container_registry:latest .
```

### 🔐 Authenticate to GHCR

```
echo "YOUR_GITHUB_PAT" | docker login ghcr.io -u YOUR_GITHUB_USERNAME --password-stdin
```

### 📤 Push the Image to GHCR

```
docker push ghcr.io/YOUR_GITHUB_USERNAME/github_container_registry:latest

```

### 📥 Pull and Run the Image

```
docker pull ghcr.io/YOUR_GITHUB_USERNAME/github_container_registry:latest
docker run -p 3000:3000 ghcr.io/YOUR_GITHUB_USERNAME/github_container_registry
```

Visit http://localhost:3000 in your browser 🚀

## 🛠️ Tech Stack

  - Node.js
  - Express.js
  - Docker
  - GitHub Container Registry (GHCR)

## Container Registry Comparison

| Feature         | **GHCR**                          | **Docker Hub**              | **AWS ECR**                  |
| --------------- | --------------------------------- | --------------------------- | ---------------------------- |
| **Pricing**     | Free for public & limited private | Free with rate limits       | Pay-as-you-go                |
| **Integration** | Native GitHub Actions             | Docker CLI & ecosystem      | Deep AWS service integration |
| **Security**    | GitHub token-based access         | Basic auth                  | IAM roles & policies         |
| **Best For**    | GitHub-first teams & solo devs    | Open-source & Docker-native | Large-scale AWS projects     |


✅ **Tip**: Replace all `YOUR_GITHUB_USERNAME` and `YOUR_GITHUB_PAT` with your actual GitHub credentials.
