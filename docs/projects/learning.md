# 📚 Learning & Tutorials

Educational resources, hands-on laboratories, and comprehensive tutorials designed to help developers master new technologies and programming languages.

## 🔧 Programming Language Labs

### [golang_lab](https://github.com/ly2xxx/golang_lab)
**Hands-on Golang Tutorial Laboratory**

A comprehensive, interactive learning environment for mastering the Go programming language through practical exercises and real-world examples.

- **Tech Stack:** Go, Hands-on Exercises, Documentation
- **Features:** Progressive tutorials, practical examples, best practices
- **Status:** Active Learning Resource
- **License:** MIT
- **Target Audience:** Beginner to Intermediate Go developers

!!! tip "Learning Path"
    - **Fundamentals** - Syntax, data types, control structures
    - **Concurrency** - Goroutines, channels, and synchronization
    - **Web Development** - HTTP servers, APIs, and middleware
    - **Testing** - Unit testing, benchmarking, and best practices
    - **Real Projects** - Building complete applications from scratch

---

### [py_playground](https://github.com/ly2xxx/py_playground)
**Python Experimentation Playground**

Interactive Python learning environment with Jupyter notebooks for exploring Python concepts, libraries, and data science techniques.

- **Tech Stack:** Jupyter Notebook, Python, Data Science Libraries
- **Features:** Interactive notebooks, code examples, visualization demos
- **Status:** Active Learning Resource
- **Focus:** Python programming and data analysis

!!! note "Playground Topics"
    - **Core Python** - Language fundamentals and advanced features
    - **Data Science** - NumPy, Pandas, Matplotlib exploration
    - **Web Development** - Flask, FastAPI examples
    - **Automation** - Scripting and task automation tutorials

---

## 🔄 CI/CD Tutorials

### [gitlab_lab](https://github.com/ly2xxx/gitlab_lab)
**GitLab CI/CD Hands-on Laboratory**

Comprehensive tutorial and learning environment for mastering GitLab CI/CD pipelines, automation, and DevOps practices.

- **Tech Stack:** Python, GitLab CI/CD, YAML, Docker
- **Features:** Pipeline examples, hands-on exercises, best practices
- **Status:** Active Tutorial
- **Focus:** Continuous integration and deployment workflows

!!! tip "Tutorial Modules"
    - **Pipeline Basics** - Understanding .gitlab-ci.yml syntax and structure
    - **Stages & Jobs** - Building multi-stage deployment workflows
    - **Docker Integration** - Container-based CI/CD pipelines
    - **Testing Automation** - Automated test execution and reporting
    - **Deployment Strategies** - Blue-green, canary, and rolling deployments

*Also see: [Development Tools](dev-tools.md#gitlab_lab) for related GitLab automation*

---

## ☁️ Infrastructure & Cloud Labs

### [okd](https://github.com/ly2xxx/okd)
**OKD Homelab Setup Guide**

Comprehensive guide and automation scripts for setting up OKD (OpenShift Kubernetes Distribution) in a homelab environment.

- **Tech Stack:** PowerShell, Kubernetes, OKD, Infrastructure
- **Features:** Installation guides, configuration scripts, troubleshooting
- **Status:** Documentation
- **Focus:** Self-hosted Kubernetes cluster setup

!!! info "Homelab Setup"
    - **OKD Installation** - Step-by-step deployment guide
    - **Cluster Configuration** - Network, storage, and resource setup
    - **Application Deployment** - Sample application deployment workflows
    - **Monitoring & Maintenance** - Cluster health and updates

---

### [iac_poc](https://github.com/ly2xxx/iac_poc)
**Infrastructure as Code Tutorial**

Proof-of-concept and learning resource for Infrastructure as Code practices using modern IaC tools and methodologies.

- **Tech Stack:** HTML, Terraform, Ansible, IaC Tools
- **Features:** Tutorial examples, best practices, hands-on labs
- **Status:** Tutorial
- **License:** Other
- **Focus:** Automated infrastructure provisioning

!!! abstract "IaC Concepts"
    - **Declarative Configuration** - Define desired infrastructure state
    - **Version Control** - Track infrastructure changes in Git
    - **Automation** - Automated provisioning and updates
    - **Consistency** - Reproducible infrastructure deployments

*Also see: [Development Tools](dev-tools.md#iac_poc) for automation tooling*

---

## 📖 Comprehensive Tutorials

#### Course Structure

=== "Module 1: Basics"
    
    ```go
    // Getting started with Go fundamentals
    package main
    
    import "fmt"
    
    func main() {
        fmt.Println("Welcome to Go Lab!")
    }
    ```
    
    - Variables and data types
    - Functions and methods
    - Structs and interfaces
    - Error handling patterns

=== "Module 2: Concurrency"
    
    ```go
    // Exploring Go's concurrency model
    func main() {
        ch := make(chan string)
        go worker(ch)
        message := <-ch
        fmt.Println(message)
    }
    ```
    
    - Goroutines and channels
    - Select statements
    - Mutex and sync package
    - Worker pool patterns

=== "Module 3: Web Development"
    
    ```go
    // Building HTTP services
    http.HandleFunc("/api/hello", handleHello)
    log.Fatal(http.ListenAndServe(":8080", nil))
    ```
    
    - HTTP servers and clients
    - REST API development
    - Middleware patterns
    - Database integration

=== "Module 4: Advanced Topics"
    
    - Reflection and interfaces
    - Performance optimization
    - Deployment strategies
    - Testing methodologies

## 📖 Comprehensive Tutorials

### Interactive Learning Features

Each tutorial includes comprehensive learning materials:

#### Code Examples
- **Runnable Code** - All examples can be executed directly
- **Progressive Complexity** - From simple to advanced concepts
- **Real-world Applications** - Practical use cases and scenarios
- **Best Practices** - Industry-standard coding patterns

#### Hands-on Exercises
- **Guided Projects** - Step-by-step project development
- **Challenge Problems** - Test your understanding
- **Solution Walkthroughs** - Detailed explanations
- **Code Reviews** - Learn from common mistakes

#### Documentation & Resources
- **API References** - Comprehensive function and method documentation
- **External Resources** - Links to official documentation and community resources
- **Troubleshooting** - Common issues and solutions
- **Community Support** - Discussion forums and help channels

## 🎓 Learning Methodology

### Structured Learning Approach

The tutorials follow a proven educational methodology:

#### 1. Conceptual Introduction
- **Theory First** - Understand the why before the how
- **Visual Aids** - Diagrams and illustrations for complex concepts
- **Real-world Context** - Practical applications and use cases

#### 2. Guided Practice
- **Step-by-step** - Incremental skill building
- **Immediate Feedback** - Quick validation of understanding
- **Error Analysis** - Learn from mistakes and debugging

#### 3. Independent Application
- **Project-based Learning** - Build complete applications
- **Creative Challenges** - Open-ended problem solving
- **Portfolio Development** - Create showcase-worthy projects

### Learning Resources

=== "Documentation"
    
    - **Comprehensive Guides** - In-depth topic coverage
    - **API References** - Function and method documentation
    - **Quick References** - Cheat sheets and syntax guides
    - **Glossaries** - Technical term definitions

=== "Interactive Content"
    
    - **Code Playgrounds** - Browser-based code execution
    - **Interactive Tutorials** - Guided learning experiences
    - **Video Walkthroughs** - Visual learning supplements
    - **Live Demos** - Working application examples

=== "Practice Materials"
    
    - **Exercise Sets** - Skill-building practice problems
    - **Project Templates** - Starting points for applications
    - **Test Suites** - Automated validation of solutions
    - **Code Challenges** - Advanced problem-solving exercises

## 🛠️ Development Environment Setup

### Prerequisites and Setup

Each learning resource includes comprehensive setup instructions:

#### System Requirements
```bash
# Go installation and setup
$ go version
go version go1.21.0 linux/amd64

# Development tools
$ git --version
$ code --version  # VS Code (recommended)
```

#### Environment Configuration
```bash
# Clone the learning repository
git clone https://github.com/ly2xxx/golang_lab.git
cd golang_lab

# Install dependencies
go mod tidy

# Run example code
go run examples/hello-world/main.go
```

#### IDE Integration
- **VS Code Extensions** - Go language support and debugging
- **IntelliJ/GoLand** - Full-featured IDE configuration
- **Vim/Neovim** - Terminal-based development setup
- **Online IDEs** - Browser-based development options

## 🎯 Learning Objectives

### Skill Development Goals

Upon completion of the tutorials, learners will achieve:

#### Technical Proficiency
- **Language Mastery** - Deep understanding of Go syntax and idioms
- **Standard Library** - Proficiency with core Go packages
- **Concurrency Patterns** - Expertise in Go's concurrency model
- **Testing Skills** - Comprehensive testing and benchmarking abilities

#### Practical Applications
- **Web Services** - Build scalable HTTP APIs and web applications
- **CLI Tools** - Create command-line utilities and tools
- **System Programming** - Develop system-level applications
- **Microservices** - Design and implement microservice architectures

#### Professional Development
- **Code Quality** - Write maintainable, readable, and efficient code
- **Debugging Skills** - Identify and resolve issues effectively
- **Performance Optimization** - Profile and optimize application performance
- **Deployment** - Deploy applications to production environments

## 📊 Progress Tracking

### Learning Analytics

Track your progress through comprehensive metrics:

- **Completion Rates** - Module and exercise completion tracking
- **Skill Assessments** - Regular knowledge verification
- **Project Portfolio** - Showcase of completed projects
- **Community Engagement** - Participation in discussions and code reviews

### Certification and Recognition

- **Completion Certificates** - Verify tutorial completion
- **Skill Badges** - Recognize specific competencies
- **Portfolio Projects** - Showcase real-world applications
- **Community Contributions** - Recognition for helping others

## 🤝 Community Learning

### Collaborative Features

- **Discussion Forums** - Ask questions and share insights
- **Code Review** - Peer feedback on projects and exercises
- **Study Groups** - Collaborative learning opportunities
- **Mentorship** - Connect with experienced developers

### Contribution Opportunities

- **Content Creation** - Contribute new tutorials and examples
- **Bug Reports** - Help improve tutorial quality
- **Feature Requests** - Suggest new learning content
- **Community Moderation** - Help maintain a positive learning environment

## 🔮 Future Learning Resources

Planned expansions to the learning platform:

- **Advanced Go Topics** - Generics, reflection, and advanced patterns
- **Additional Languages** - Python, Rust, and JavaScript tutorials
- **Framework-Specific** - React, FastAPI, and other framework guides
- **DevOps Integration** - Docker, Kubernetes, and deployment tutorials

---

*All learning resources are designed to provide practical, hands-on experience with immediate application to real-world development scenarios.*