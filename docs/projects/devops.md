# 🔧 DevOps & Infrastructure

CI/CD pipelines, cloud deployments, Kubernetes/OpenShift, Infrastructure as Code, and security scanning.

**Total Projects:** 9 | **Stars:** 1

---

## 🌟 Featured Projects

### [gitlab_lab](https://github.com/ly2xxx/gitlab_lab)
**GitLab CI/CD hands-on tutorial**

Comprehensive hands-on tutorial for learning GitLab pipelines, runners, and deployment strategies. Step-by-step labs covering everything from basics to advanced patterns.

- **Tech Stack:** Python, GitLab CI/CD, Docker, Kubernetes
- **Features:**
  - Complete pipeline examples
  - Runner configuration guides
  - Multi-stage deployments
  - Security scanning integration
  - Artifact management
- **Status:** 🟢 Active (Updated: 2025-09-24)
- **Audience:** DevOps engineers, developers learning CI/CD
- **Structure:** Organized lab exercises with solutions

---

### [gitlab-runner-poc](https://github.com/ly2xxx/gitlab-runner-poc) ⭐ 1
**Simulate GitLab pipeline locally**

Run and test GitLab CI/CD pipelines locally before pushing to the server. Essential tool for pipeline development and debugging.

- **Tech Stack:** GitLab Runner, Docker
- **Features:**
  - Local pipeline execution
  - Fast iteration cycles
  - Debug mode support
  - No server dependency
- **Status:** 🟢 Active (Updated: 2025-07-16)
- **Stars:** ⭐
- **Use Cases:** Pipeline development, debugging, testing

---

### [okd](https://github.com/ly2xxx/okd)
**OpenShift Kubernetes Distribution homelab setup**

Step-by-step guide for setting up OKD (OpenShift Kubernetes Distribution) homelab on Windows PC using OpenShift Local (CRC).

- **Tech Stack:** PowerShell, OpenShift/OKD, Kubernetes
- **Features:**
  - Windows installation guide
  - CRC (CodeReady Containers) setup
  - Networking configuration
  - Sample deployments
  - Troubleshooting tips
- **Status:** 🟢 Active (Updated: 2025-10-12)
- **Platform:** Windows PC homelab
- **Learning Path:** Kubernetes → OpenShift fundamentals

---

## 🚀 GitLab CI/CD Projects

### [gitlab-poc](https://github.com/ly2xxx/gitlab-poc)
**GitLab experiments and POCs**

Collection of GitLab CI/CD experiments exploring various pipeline patterns, integrations, and best practices.

- **Tech Stack:** Python, GitLab CI
- **Topics:** Pipeline optimization, integration testing, deployment patterns
- **Status:** 🟡 Stable (Updated: 2025-05-28)

---

### [evergreen](https://github.com/ly2xxx/evergreen)
**Evergreen GitLab projects**

Long-term maintained GitLab projects demonstrating production-grade CI/CD practices.

- **Tech Stack:** Python, GitLab
- **Focus:** Production patterns, maintenance strategies
- **Status:** 🟡 Stable (Updated: 2025-10-01)

---

## ☁️ Cloud & Azure

### [azure-flask-cv](https://github.com/ly2xxx/azure-flask-cv)
**Azure Flask computer vision deployment**

Flask-based computer vision application deployed to Azure. Demonstrates Azure App Service deployment with ML capabilities.

- **Tech Stack:** Jupyter Notebook, Flask, Azure App Service, Computer Vision
- **Features:** Azure deployment, CV model serving, REST API
- **Status:** 🔴 Archived (Updated: 2023-12-06)
- **Learning:** Azure SDLC, Flask deployment, CV APIs

---

### [msdocs-python-flask-webapp-quickstart](https://github.com/ly2xxx/msdocs-python-flask-webapp-quickstart)
**Azure full SDLC exercise**

Microsoft documentation sample adapted for learning complete Azure software development lifecycle.

- **Tech Stack:** HTML, Flask, Azure
- **Purpose:** Practice Azure DevOps, CI/CD, deployment
- **Status:** 🔴 Archived (Updated: 2023-12-03)
- **Source:** Microsoft official documentation

---

## 🏗️ Infrastructure as Code

### [iac_poc](https://github.com/ly2xxx/iac_poc)
**Infrastructure as Code proof-of-concept**

Home lab tutorial based on VirtualizationHowTo guides. Demonstrates IaC principles with practical homelab examples.

- **Tech Stack:** HTML, Terraform/Ansible
- **Topics:** Virtualization, automation, configuration management
- **Status:** 🟡 Stable (Updated: 2025-07-25)
- **Reference:** VirtualizationHowTo tutorials

---

## 🔒 Security

### [gitleaks-poc](https://github.com/ly2xxx/gitleaks-poc)
**GitLeaks secret scanning**

Proof-of-concept for detecting secrets, passwords, and API keys in Git repositories using GitLeaks.

- **Tech Stack:** HTML, GitLeaks
- **Features:**
  - Secret detection patterns
  - Pre-commit hooks
  - CI/CD integration
  - Custom rule configuration
- **Status:** 🟡 Stable (Updated: 2025-06-30)
- **Security:** Prevent credential leaks, scan history

---

## 📊 Project Matrix

| Project | Focus | Complexity | Status | Best For |
|---------|-------|------------|--------|----------|
| gitlab_lab | Tutorial | ⭐⭐ | 🟢 Active | Learning GitLab |
| gitlab-runner-poc | Local testing | ⭐⭐⭐ | 🟢 Active | Pipeline dev |
| okd | Kubernetes | ⭐⭐⭐⭐ | 🟢 Active | K8s learning |
| gitlab-poc | Experiments | ⭐⭐ | 🟡 Stable | Pattern reference |
| evergreen | Production | ⭐⭐⭐ | 🟡 Stable | Best practices |
| iac_poc | IaC | ⭐⭐⭐ | 🟡 Stable | Homelab setup |
| gitleaks-poc | Security | ⭐⭐ | 🟡 Stable | Secret scanning |
| azure-flask-cv | Cloud ML | ⭐⭐⭐ | 🔴 Archived | Azure reference |
| msdocs-flask | Azure basics | ⭐ | 🔴 Archived | Azure quickstart |

---

## 🎯 Learning Paths

### Path 1: GitLab CI/CD Mastery
1. **gitlab_lab** - Start with fundamentals
2. **gitlab-runner-poc** - Learn local testing
3. **gitlab-poc** - Explore advanced patterns
4. **evergreen** - Study production examples
5. **gitleaks-poc** - Add security scanning

### Path 2: Kubernetes Journey
1. **iac_poc** - Understand infrastructure concepts
2. **okd** - Set up OpenShift homelab
3. Deploy sample apps from **gitlab_lab**

### Path 3: Cloud Deployment
1. **msdocs-flask** - Azure basics
2. **azure-flask-cv** - ML deployment
3. Integrate with **gitlab_lab** pipelines

---

## 🔧 Key Technologies

### CI/CD
- **GitLab CI/CD** - Primary automation platform
- **GitLab Runner** - Pipeline execution
- **Docker** - Containerization
- **Kubernetes** - Orchestration

### Cloud Platforms
- **Azure App Service** - PaaS deployments
- **Azure DevOps** - CI/CD pipelines
- **OpenShift/OKD** - Enterprise Kubernetes

### Security
- **GitLeaks** - Secret scanning
- **SAST/DAST** - Security testing
- **Container scanning** - Vulnerability detection

### Infrastructure
- **Terraform** - Infrastructure as Code
- **Ansible** - Configuration management
- **PowerShell** - Windows automation

---

## 🚀 Quick Starts

### Local GitLab Pipeline Testing

```bash
# Clone gitlab-runner-poc
git clone https://github.com/ly2xxx/gitlab-runner-poc.git
cd gitlab-runner-poc

# Install GitLab Runner
# (See README for OS-specific instructions)

# Run pipeline locally
gitlab-runner exec docker test
```

### OpenShift Homelab Setup

```powershell
# Clone okd repository
git clone https://github.com/ly2xxx/okd.git
cd okd

# Follow step-by-step guide in README
# Install CRC (CodeReady Containers)
# Configure networking
# Deploy sample apps
```

---

## 📚 Resources

### GitLab
- [GitLab CI/CD Documentation](https://docs.gitlab.com/ee/ci/)
- [GitLab Runner Docs](https://docs.gitlab.com/runner/)
- [GitLab CI/CD Examples](https://docs.gitlab.com/ee/ci/examples/)

### Kubernetes/OpenShift
- [OKD Documentation](https://docs.okd.io/)
- [OpenShift Local Guide](https://developers.redhat.com/products/openshift-local/overview)
- [Kubernetes Tutorials](https://kubernetes.io/docs/tutorials/)

### Security
- [GitLeaks GitHub](https://github.com/gitleaks/gitleaks)
- [OWASP DevSecOps](https://owasp.org/www-project-devsecops-guideline/)

---

## 🔗 Integration Opportunities

- **AI/ML:** Deploy `aidev` or `rag_chat_opensource_llm` using GitLab CI/CD
- **Web Apps:** Use pipelines for `hrtoolkit` or `treasure` deployments
- **Security:** Integrate `gitleaks-poc` into all Git repositories

---

*Updated: 2026-02-07*
