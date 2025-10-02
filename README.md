<div align="left" style="position: relative;">
<img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" align="right" width="30%" style="margin: -20px 0 0 20px;">
<h1>MLOPS-PROJECT</h1>
<p align="left">
	<img src="https://img.shields.io/github/last-commit/MarcGeorgeML/MLOPS-PROJECT?style=default&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/MarcGeorgeML/MLOPS-PROJECT?style=default&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/MarcGeorgeML/MLOPS-PROJECT?style=default&color=0080ff" alt="repo-language-count">
</p>
<p align="left"><!-- default option, no dependency badges. -->
</p>
<p align="left">
	<!-- default option, no dependency badges. -->
</p>
</div>
<br clear="right">

##  Table of Contents

- [ Overview](#-overview)
- [ Features](#-features)
- [ Project Structure](#-project-structure)
- [ Getting Started](#-getting-started)
  - [ Prerequisites](#-prerequisites)
  - [ Installation](#-installation)
  - [ Usage](#-usage)
  - [ Testing](#-testing)
- [ Project Roadmap](#-project-roadmap)
- [ Contributing](#-contributing)
- [ Acknowledgments](#-acknowledgments)

---

##  Overview

<code>❯ An end-to-end MLOps project that builds, tests, packages, and deploys a machine learning service on AWS using containerized workflows and automated CI/CD. The pipeline covers data ingestion (MongoDB), training and artifact versioning (S3), image packaging (Docker + ECR), and production inference (FastAPI on EC2) with continuous deployment via GitHub Actions. The repository includes testing with Pytest, infrastructure-conscious practices, and a minimal frontend (HTML/CSS) for interacting with the API.</code>

---

##  Features

Here’s a concise GitHub-ready overview plus a clear feature list.
- Data pipeline
  - Ingestion and persistence in MongoDB with scriptable preprocessing and validation.
  - Clear separation of raw, processed, and model-ready data steps.

- Model training and artifacts
  - Containerized training jobs for reproducibility across dev and cloud.
  - Model serialization and artifact storage in AWS S3.
  - Configurable training parameters and deterministic runs.

- API service (inference)
  - FastAPI-based REST endpoints for low-latency predictions.
  - Automatic API schema/docs via OpenAPI/Swagger.
  - Stateless service design pulling model artifacts from S3/ECR.

- Containerization
  - Dockerfile(s) for training and serving.
  - Consistent, portable runtime across local and cloud environments.

- CI/CD automation
  - GitHub Actions pipeline: test → build → push image to ECR → deploy on EC2.
  - Branch-based triggers and reusable workflow steps.
  - Secure secret management for cloud credentials and environment variables.

- Cloud deployment
  - AWS ECR for versioned Docker images.
  - AWS EC2 as the production host running the containerized FastAPI app.
  - AWS S3 for artifact storage and decoupled model delivery.

- Testing and quality
  - Pytest suites covering data, utils, and inference logic.
  - Pre-deploy checks to prevent regressions reaching production.

- Frontend
  - Lightweight HTML/CSS interface to submit requests and visualize results.
  - Developer-friendly docs view via FastAPI /docs.

- Operations and reliability
  - Environment-specific configuration (dev/prod) via variables.
  - Logs and errors surfaced from API/container for faster debugging.
  - Clear runbooks for setup, local dev, and deployment.

- Developer experience
  - Makefile or task scripts for common commands (optional).
  - Structured repo layout for components (data, src, models, infra, CI).
  - Readable, step-by-step setup instructions.


---

##  Project Structure

```sh
└── MLOPS-PROJECT/
    ├── .github
    │   └── workflows
    ├── Dockerfile
    ├── README.md
    ├── app.py
    ├── config
    │   ├── model.yaml
    │   └── schema.yaml
    ├── crashcourse.txt
    ├── demo.py
    ├── logs
    │   ├── 10_01_2025_18_03_56.log
    │   ├── 10_01_2025_18_10_35.log
    │   ├── 10_01_2025_18_16_38.log
    │   ├── 10_01_2025_19_01_40.log
    │   ├── 10_01_2025_19_03_59.log
    │   ├── 10_01_2025_19_09_16.log
    │   └── 10_01_2025_20_26_04.log
    ├── notebook
    │   ├── data.csv
    │   ├── exp-notebook.ipynb
    │   └── mongoDB_demo.ipynb
    ├── persistent-terminals.log
    ├── projectflow.txt
    ├── pyproject.toml
    ├── requirements.txt
    ├── setup.py
    ├── src
    │   ├── __init__.py
    │   ├── __pycache__
    │   ├── cloud_storage
    │   ├── components
    │   ├── configuration
    │   ├── constants
    │   ├── data_access
    │   ├── entity
    │   ├── exception
    │   ├── logger
    │   ├── pipline
    │   └── utils
    ├── src.egg-info
    │   ├── PKG-INFO
    │   ├── SOURCES.txt
    │   ├── dependency_links.txt
    │   └── top_level.txt
    ├── static
    │   └── css
    ├── template.py
    └── templates
        └── vehicledata.html
```

##  Getting Started

###  Prerequisites

Before getting started with MLOPS-PROJECT, ensure your runtime environment meets the following requirements:

- **Programming Language:** Python
- **Package Manager:** Pip
- **Container Runtime:** Docker


###  Installation

Install MLOPS-PROJECT using one of the following methods:

**Build from source:**

1. Clone the MLOPS-PROJECT repository:
```sh
❯ git clone https://github.com/MarcGeorgeML/MLOPS-PROJECT
```

2. Navigate to the project directory:
```sh
❯ cd MLOPS-PROJECT
```

3. Install the project dependencies:


**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ pip install -r requirements.txt
```


**Using `docker`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```sh
❯ docker build -t MarcGeorgeML/MLOPS-PROJECT .
```




###  Usage
Run MLOPS-PROJECT using the following command:
**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ python {entrypoint}
```


**Using `docker`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Docker-2CA5E0.svg?style={badge_style}&logo=docker&logoColor=white" />](https://www.docker.com/)

```sh
❯ docker run -it {image_name}
```


###  Testing
Run the test suite using the following command:
**Using `pip`** &nbsp; [<img align="center" src="https://img.shields.io/badge/Pip-3776AB.svg?style={badge_style}&logo=pypi&logoColor=white" />](https://pypi.org/project/pip/)

```sh
❯ pytest
```


---
##  Project Roadmap

- [X] **`Task 1`**: <strike>Implement basic ML Pipeline.</strike>
- [X] **`Task 2`**: Implement validation, evaluation and CI/CD.
- [X] **`Task 3`**: Deploy on AWS.

---

##  Contributing

- **💬 [Join the Discussions](https://github.com/MarcGeorgeML/MLOPS-PROJECT/discussions)**: Share your insights, provide feedback, or ask questions.
- **🐛 [Report Issues](https://github.com/MarcGeorgeML/MLOPS-PROJECT/issues)**: Submit bugs found or log feature requests for the `MLOPS-PROJECT` project.
- **💡 [Submit Pull Requests](https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/main/CONTRIBUTING.md)**: Review open PRs, and submit your own PRs.

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your github account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone https://github.com/MarcGeorgeML/MLOPS-PROJECT
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to github**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<summary>Contributor Graph</summary>
<br>
<p align="left">
   <a href="https://github.com{/MarcGeorgeML/MLOPS-PROJECT/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=MarcGeorgeML/MLOPS-PROJECT">
   </a>
</p>
</details>

---

##  Acknowledgments

- Special thanks to **Vikash Das** for the excellent MLOps tutorial that inspired this project. Check out the original tutorial: [YT-MLops-Proj1](https://github.com/vikashishere/YT-MLops-Proj1)

---
