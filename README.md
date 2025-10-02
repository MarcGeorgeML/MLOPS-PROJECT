<div align="left" style="position: relative;">
<img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" align="right" width="30%" style="margin: -20px 0 0 20px;">
<h1>MLOPS-PROJECT</h1>
<p align="left">
	<em><code>❯ REPLACE-ME</code></em>
</p>
<p align="left">
	<img src="https://img.shields.io/github/license/MarcGeorgeML/MLOPS-PROJECT?style=default&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
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
  - [ Project Index](#-project-index)
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

<code>❯ Here’s a concise GitHub-ready overview plus a clear feature list.
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
</code>

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


###  Project Index
<details open>
	<summary><b><code>MLOPS-PROJECT/</code></b></summary>
	<details> <!-- __root__ Submodule -->
		<summary><b>__root__</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/crashcourse.txt'>crashcourse.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/template.py'>template.py</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/app.py'>app.py</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/requirements.txt'>requirements.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/pyproject.toml'>pyproject.toml</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/demo.py'>demo.py</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/projectflow.txt'>projectflow.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/setup.py'>setup.py</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/Dockerfile'>Dockerfile</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			</table>
		</blockquote>
	</details>
	<details> <!-- .github Submodule -->
		<summary><b>.github</b></summary>
		<blockquote>
			<details>
				<summary><b>workflows</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/.github/workflows/aws.yaml'>aws.yaml</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
		</blockquote>
	</details>
	<details> <!-- src Submodule -->
		<summary><b>src</b></summary>
		<blockquote>
			<details>
				<summary><b>configuration</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/configuration/mongo_db_connection.py'>mongo_db_connection.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/configuration/aws_connection.py'>aws_connection.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>data_access</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/data_access/MLOPsProjectData.py'>MLOPsProjectData.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>components</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/model_pusher.py'>model_pusher.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/data_ingestion.py'>data_ingestion.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/data_transformation.py'>data_transformation.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/model_trainer.py'>model_trainer.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/model_evaluation.py'>model_evaluation.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/components/data_validation.py'>data_validation.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>entity</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/entity/s3_estimator.py'>s3_estimator.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/entity/artifact_entity.py'>artifact_entity.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/entity/config_entity.py'>config_entity.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/entity/estimator.py'>estimator.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>cloud_storage</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/cloud_storage/aws_storage.py'>aws_storage.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>pipline</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/pipline/prediction_pipeline.py'>prediction_pipeline.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/pipline/training_pipeline.py'>training_pipeline.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
			<details>
				<summary><b>utils</b></summary>
				<blockquote>
					<table>
					<tr>
						<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src/utils/main_utils.py'>main_utils.py</a></b></td>
						<td><code>❯ REPLACE-ME</code></td>
					</tr>
					</table>
				</blockquote>
			</details>
		</blockquote>
	</details>
	<details> <!-- templates Submodule -->
		<summary><b>templates</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/templates/vehicledata.html'>vehicledata.html</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			</table>
		</blockquote>
	</details>
	<details> <!-- config Submodule -->
		<summary><b>config</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/config/schema.yaml'>schema.yaml</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/config/model.yaml'>model.yaml</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			</table>
		</blockquote>
	</details>
	<details> <!-- notebook Submodule -->
		<summary><b>notebook</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/notebook/exp-notebook.ipynb'>exp-notebook.ipynb</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/notebook/mongoDB_demo.ipynb'>mongoDB_demo.ipynb</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			</table>
		</blockquote>
	</details>
	<details> <!-- src.egg-info Submodule -->
		<summary><b>src.egg-info</b></summary>
		<blockquote>
			<table>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src.egg-info/PKG-INFO'>PKG-INFO</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src.egg-info/top_level.txt'>top_level.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src.egg-info/dependency_links.txt'>dependency_links.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			<tr>
				<td><b><a href='https://github.com/MarcGeorgeML/MLOPS-PROJECT/blob/master/src.egg-info/SOURCES.txt'>SOURCES.txt</a></b></td>
				<td><code>❯ REPLACE-ME</code></td>
			</tr>
			</table>
		</blockquote>
	</details>
</details>

---
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
