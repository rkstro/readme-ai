<p align="center">
  <img src="https://img.icons8.com/?size=512&id=55494&format=png" width="99">
  <img src="https://img.icons8.com/?size=512&id=kTuxVYRKeKEY&format=png" width="99">
</p>
<h1 align="center">README-AI</h1>
<p align="center">
    <em>Automated README file generator, powered by LLM APIs</em>
</p>
<p align="center">
  <a href="https://github.com/eli64s/readme-ai/actions">
    <img src="https://img.shields.io/github/actions/workflow/status/eli64s/readme-ai/release-pipeline.yml?logo=githubactions&label=CICD&logoColor=white&color=c125ff"
    alt="github-actions">
  </a>
  <a href="https://app.codecov.io/gh/eli64s/readme-ai">
    <img src="https://img.shields.io/codecov/c/github/eli64s/readme-ai?logo=codecov&logoColor=white&label=Coverage&color=c125ff"
    alt="codecov">
  </a>
  <a href="https://pypi.python.org/pypi/readmeai/">
    <img src="https://img.shields.io/pypi/v/readmeai?logo=PyPI&logoColor=white&label=PyPI&color=c125ff" alt="pypi-version">
  </a>
  <a href="https://www.pepy.tech/projects/readmeai">
    <img src="https://img.shields.io/pepy/dt/readmeai?logo=Python&logoColor=white&label=Downloads&color=c125ff"
    alt="pepy-total-downloads">
  </a>
</p>

<!--
<p align="center">
  <img src="./examples/images/readmeai-logo.jpg" width="55%" alt="readme-ai-logo">
<p align="center">
    <em>Automated <code>README</code> file generator, powered by large language model APIs</em>
</p>
<p align="center">
  <a href="https://github.com/eli64s/readme-ai/actions">
    <img src="https://img.shields.io/github/actions/workflow/status/eli64s/readme-ai/release-pipeline.yml?logo=githubactions&label=CICD&logoColor=white&color=0041C2&labelColor=6C6C6C"
    alt="github-actions">
  </a>
  <a href="https://app.codecov.io/gh/eli64s/readme-ai">
    <img src="https://img.shields.io/codecov/c/github/eli64s/readme-ai?logo=codecov&logoColor=white&label=Coverage&color=0041C2&labelColor=6C6C6C"
    alt="codecov">
  </a>
  <a href="https://pypi.python.org/pypi/readmeai/">
    <img src="https://img.shields.io/pypi/v/readmeai?logo=PyPI&logoColor=white&label=PyPI&color=0041C2&labelColor=6C6C6C"
    alt="pypi-version">
  </a>
  <a href="https://www.pepy.tech/projects/readmeai">
    <img src="https://img.shields.io/pepy/dt/readmeai?logo=PyPI&logoColor=white&label=Downloads&color=0041C2&labelColor=6C6C6C"
    alt="pepy-total-downloads">
  </a>
  <a href="https://opensource.org/license/mit/">
    <img src="https://img.shields.io/github/license/eli64s/readme-ai?logo=opensourceinitiative&logoColor=white&label=License&color=0041C2&labelColor=6C6C6C"
    alt="license">
  </a>
</p>
-->

<!-- TABLE OF CONTENTS -->
<details>
  <summary><h4>Table of Contents</h4></summary>

- [📍 Overview](#-overview)
- [🤖 Demo](#-demo)
- [🔮 Features](#-features)
- [🧑‍🎨 Examples](#-example-readmes)
- [🚀 Getting Started](#-getting-started)
  - [⚙️ Install](#️-installation)
  - [🧑‍💻 Usage](#-running-readme-ai)
  - [🧪 Tests](#-tests)
- [🧩 Configuration](#-configuration)
- [🛠 Project Roadmap](#-project-roadmap)
- [🤝 Contributing](#-contributing)
</details>

---

## 📍 Overview

***Objective***

Readme-ai is a developer tool that auto-generates README.md files using a combination of data extraction and generative ai. Simply provide a repository URL or local path to your codebase and a well-structured and detailed README file will be generated for you.

***Motivation***

Streamlines documentation creation and maintenance, enhancing developer productivity. This project aims to enable all skill levels, across all domains, to better understand, use, and contribute to open-source software.<br>

> [!IMPORTANT]
>
> <sub>Readme-ai is currently under development with an opinionated configuration and setup. It is vital to review all generated text from the LLM API to ensure it accurately represents your project.</sub>

---

## 🤖 Demo

Standard CLI usage, providing a repository URL to generate a README file.

[readmeai-cli-demo](https://github.com/eli64s/artifacts/assets/43382407/55b8d1b9-06a7-4b1f-b6a7-aaeccdb27679
)

Generate a README file without making API calls using the `--api offline` CLI option.

[readmeai-streamlit-demo](https://github.com/eli64s/artifacts/assets/43382407/3eb39fcf-c1df-49c6-bb5c-63e141857ae3)

> [!TIP]
>
> <sub>Offline mode is useful for generating a boilerplate README at no cost. View the offline README.md example [here!](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-offline.md)</sub>

---

## 🔮 Features

Built with flexibility in mind, readme-ai allows users to customize various aspects of the README using CLI options. Content is generated using a combination of data extraction and making a few calls to LLM APIs.

Currently, four sections of the README file are generated using LLMs:

> i. **Header**: Project slogan that describes the repository in an engaging way.<br>
> ii. **Overview**: Provides an intro to the project's core use-case and value proposition.<br>
> iii. **Features**: Markdown table containing details about the project's technical components.<br>
> iv. **Modules**: Codebase file summaries are generated and formatted into markdown tables.<br>

All other content is extracted from processing and analyzing repository metadata and files.

### Customizable Header

The header section is built using repository metadata and CLI options. Key features include:
- **Badges**: Svg icons that represent codebase metadata, provided by [shields.io](https://shields.io/) and [skill-icons](https://github.com/tandpfun/skill-icons).
- **Project Logo**: Select a project logo image from the base set or provide your image.
- **Project Slogan**: Catch phrase that describes the project, generated by generative ai.
- **Table of Contents/Quick Links**: Links to the different sections of the README file.

See a few example headers generated by *readme-ai* below.
<table>
  <!-- row 1 -->
  <tr>
    <td colspan="2" align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-default.png" alt="default-header" width="800"/><br>
      <code>default output (no options provided to cli)</code>
    </td>
  </tr>
  <!-- row 2 -->
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-cloud.png" alt="cloud-db-logo" width="400"/><br>
      <code>--align left --badges flat-square --image cloud</code>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-gradient.png" alt="gradient-markdown-logo" width="400"/><br>
      <code>--align left --badges flat --image gradient</code>
    </td>
  </tr>
  <!-- row 3 -->
  <tr>
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-custom.png" alt="custom-logo" width="400"/><br>
      <code>--badges flat --image custom</code>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-skills.png" alt="skills-light" width="400"/><br>
      <code>--badges skills-light --image grey</code>
    </td>
  </tr>
  <tr>
  <!-- row 4 -->
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-flat-square.png" alt="readme-ai-header" width="400"/><br>
      <code>--badges flat-square</code>
    </td>
    <td align="center">
      <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/header-black.png" alt="black-logo" width="400"/><br>
      <code>--badges flat --image black</code>
    </td>
  </tr>
</table>

See the <a href="#-configuration">Configuration</a> section below for the complete list of CLI options and settings.<br>

<details closed>
  <summary>📑 Codebase Documentation</summary>
  <br>
  <table>
    <tr>
      <td>
        <b>Repository Structure</b><br>
        <p>A directory tree structure is generated using pure Python <a href="https://github.com/eli64s/readme-ai/blob/main/readmeai/markdown/tree.py">(tree.py)</a> and embedded in the README.
        </p>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/directory-tree.png" alt="directory-tree" width="700" />
      </td>
    </tr>
    <tr>
      <td style="padding-top:20px;">
        <b>Codebase Summaries</b>
        <br>
        <p>Code summaries are generated using LLMs and grouped by directory, displayed in markdown tables.</p>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/llm-summaries.png" alt="llm-summaries" width="700" />
      </td>
    </tr>
  </table>
</details>
<!-- -->
<details closed>
  <summary>📍 Overview & Features Table</summary>
  <p>The overview and features sections are generated using LLM APIs. Structured prompt templates are injected with repository metadata to help produce more accurate and relevant content.
  </p>
  <table>
    <tr>
      <td><b>Overview</b><br>
        <p>High-level introduction of the project, focused on the value proposition and use-cases, rather than technical aspects.</p>
      </td>
    </tr>
    <tr>
      <td align="center"><img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/llm-overview.png" alt="llm-overview" width="700" /></td>
    </tr>
    <tr>
      <td style="padding-top:20px;"><b>Features Table</b><br>
        <p>Describes technical components of the codebase, including architecture, dependencies, testing, integrations, and more.</p>
      </td>
    </tr>
    <tr>
      <td align="center"><img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/llm-features.png" alt="llm-features" width="700" /></td>
    </tr>
  </table>
</details>
<!-- -->
<details closed>
  <summary>🚀 Dynamic Quickstart Guides</summary>
  <br>
  <table>
    <tr>
      <td><b>Getting Started or Quick Start</b><br>
        <p>Generates structured guides for installing, running, and testing your project. These steps are created by identifying dependencies and languages used in the codebase, and mapping this data to configuration files such as the <a href="https://github.com/eli64s/readme-ai/blob/main/readmeai/settings/language_setup.toml">language_setup.toml</a> file.</p>
      </td>
    </tr>
    <tr>
      <td align="center"><img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/quickstart.png" alt="quick-start" width="700" />
      </td>
    </tr>
  </table>
</details>
<!-- -->
<details closed>
  <summary>🤝 Contributing Guidelines & More</summary>
  <br>
  <table>
    <tr>
      <td><b>Additional Sections</b><br>
        <p>The remaining README sections are built from a baseline template that includes common sections such as <code>Project Roadmap, Contributing Guidelines, License, and Acknowledgements</code>.</p>
      </td>
    </tr>
    <tr>
      <td align="center"><img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/additional-sections.png" alt="contributing-and-more" width="700" /></td>
    </tr>
    <tr>
      <td style="padding-top:20px;"><b>Contributing Guidelines</b><br>
        <p>The contributing guidelines has a dropdown that outlines a general process for contributing to your project.</p>
      </td>
    </tr>
    <tr>
      <td align="center"><img src="https://raw.githubusercontent.com/eli64s/readme-ai/main/examples/images/contributing-guidelines.png" alt="contributing-guidelines" width="700" /></td>
    </tr>
  </table>
</details>
<!-- -->
<details closed>
  <summary>🧩 Template READMEs</summary>
  <p>This feature is currently under development. The template system will allow users to generate README files in different flavors, such as ai, data, web development, etc.
  </p>
  <table>
    <tr>
      <td>
        <h3>README Template for ML & Data</h3>
        <ul>
          <li><a href="#overview">Overview</a>: Project objectives, scope, outcomes.</li>
          <li><a href="#project-structure">Project Structure</a>: Organization and components.</li>
          <li><a href="#data-preprocessing">Data Preprocessing</a>: Data sources and methods.</li>
          <li><a href="#feature-engineering">Feature Engineering</a>: Impact on model performance.</li>
          <li><a href="#model-architecture">Model Architecture</a>: Selection and development strategies.</li>
          <li><a href="#training-and-validation">Training</a>: Procedures, tuning, strategies.</li>
          <li><a href="#testing-and-evaluation">Testing and Evaluation</a>: Results, analysis, benchmarks.</li>
          <li><a href="#deployment">Deployment</a>: System integration, APIs.</li>
          <li><a href="#usage">Usage and Maintenance</a>: User guide, model upkeep.</li>
          <li><a href="#results">Results and Discussion</a>: Implications, future work.</li>
          <li><a href="#ethical-considerations">Ethical Considerations</a>: Ethics, privacy, fairness.</li>
          <li><a href="#contributing">Contributing</a>: Contribution guidelines.</li>
          <li><a href="#acknowledgements">Acknowledgements</a>: Credits, resources used.</li>
          <li><a href="#license">License</a>: Usage rights, restrictions.</li>
        </ul>
      </td>
    </tr>
  </table>
</details>

---

## 🧑‍🎨 Example READMEs

| ⭑ | **Output File 📄** | **Input Repository 📁** | **Repository Type 🔢** |
|---|-------------|------------|-----------|
| ⭑ | [readme-python.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-python.md) | [readme-ai](https://github.com/eli64s/readme-ai) | Python |
| ⭑ | [readme-typescript.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-typescript.md) | [chatgpt-app-react-ts](https://github.com/Yuberley/ChatGPT-App-React-Native-TypeScript) | TypeScript, React |
| ⭑ | [readme-postgres.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-postgres.md) | [postgres-proxy-server](https://github.com/jwills/buenavista) | Postgres, Duckdb |
| ⭑ | [readme-kotlin.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-kotlin.md) | [file.io-android-client](https://github.com/rumaan/file.io-Android-Client) | Kotlin, Android |
| ⭑ | [readme-streamlit.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-streamlit.md) | [readme-ai-streamlit](https://github.com/eli64s/readme-ai-streamlit) | Python, Streamlit |
| ⭑ | [readme-rust-c.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-rust-c.md) | [rust-c-app](https://github.com/DownWithUp/CallMon) | C, Rust |
| ⭑ | [readme-go.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-go.md) | [go-docker-app](https://github.com/olliefr/docker-gs-ping) | Go |
| ⭑ | [readme-java.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-java.md) | [java-minimal-todo](https://github.com/avjinder/Minimal-Todo) | Java |
| ⭑ | [readme-fastapi-redis.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-fastapi-redis.md) | [async-ml-inference](https://github.com/FerrariDG/async-ml-inference) | FastAPI, Redis |
| ⭑ | [readme-mlops.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-mlops.md) | [mlops-course](https://github.com/GokuMohandas/mlops-course) | Python, Jupyter |
| ⭑ | [readme-local.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-local.md) | Local Directory | Flink, Python |

<!--
| ⭑ | [readme-vertex.md](https://github.com/eli64s/readme-ai/blob/main/examples/markdown/readme-vertex.md) | Vertex AI | Google Cloud |
| ⭑ | [readme-gitlab.md]() | [gitlab](https://github.com/eli64s/flink-flow) | GitLab |
| ⭑ | [readme-bitbucket.md]() | [bitbucket](https://github.com/eli64s/flink-flow) | BitBucket |
-->

---

## 🚀 Getting Started

**Requirements**

* Python: 3.9+
* Package manager or container runtime: `pip` or `docker` recommended.
* LLM API: `OpenAI` and `Google Vertex AI` LLM APIs are currently supported.

**Repository**

A repository URL or local path to your codebase is required run readme-ai. The following are supported:
* [GitHub](https://github.com/)
* [GitLab](https://gitlab.com/)
* [Bitbucket](https://bitbucket.org/)
* [File System](https://en.wikipedia.org/wiki/File_system)

**OpenAI API Key**

An OpenAI API account and API key are needed to use readme-ai. Get started by creating an account [here](https://platform.openai.com/docs/quickstart/account-setup). Once you have an account, you can create an API key on the [API settings page](https://platform.openai.com/api-keys).

> [!WARNING]
>
> Before using readme-ai, its essential to understand the potential risks and costs associated with using AI-powered tools.
>
> * **Review Sensitive Information**: Ensure all content in your repository is free of sensitive information before running the tool. This project does not remove sensitive data from your codebase, nor from the output README file.
>
> * **API Usage Costs**: The OpenAI API is not free and costs can accumulate quickly! You will be charged for each request made by readme-ai. Be sure to monitor API usage costs using the [OpenAI API Usage Dashboard](https://platform.openai.com/account/usage).

---

### ⚙️ Installation

#### Using `pip`

> [![pip](https://img.shields.io/badge/PyPI-3775A9.svg?style=flat&logo=PyPI&logoColor=white)](https://pypi.org/project/readmeai/)
>
> ```sh
> pip install readmeai
> ```

#### Using `docker`

> [![docker](https://img.shields.io/badge/Docker-2496ED.svg?style=flat&logo=Docker&logoColor=white)](https://hub.docker.com/r/zeroxeli/readme-ai)
>
> ```sh
> docker pull zeroxeli/readme-ai:latest
> ```

#### Using `conda`

> [![conda](https://img.shields.io/badge/Anaconda-44A833.svg?style=flat&logo=Anaconda&logoColor=white)](https://anaconda.org/zeroxeli/readmeai)
>
> ```sh
> conda install -c conda-forge readmeai
> ```

<details closed>
<summary>
  <h4>From <code>source</code></h4>
</summary>

> Clone repository and change directory.
>
> ```console
> $ git clone https://github.com/eli64s/readme-ai
> $ cd readme-ai
> ```

#### Using `bash`
>
> [![bash](https://img.shields.io/badge/GNU%20Bash-4EAA25.svg?style=flat&logo=GNU-Bash&logoColor=white)](https://www.gnu.org/software/bash/)
>
> ```console
> $ bash setup/setup.sh
> ```

#### Using `poetry`
> [![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
>
> ```console
> $ poetry install
> ```

* <sub>Similiary you can use `pipenv` or `pip` to install the requirements.txt.</sub>

</details>

> [!TIP]
>
> [![pipx](https://img.shields.io/badge/pipx-2CFFAA.svg?style=flat&logo=pipx&logoColor=black)](https://pipxproject.github.io/pipx/installation/)
>
> <sub>Use [pipx](https://pipx.pypa.io/stable/installation/) to install and run Python command-line applications without causing dependency conflicts with other packages installed on the system.</sub>

---

### 🧑‍💻 Running `readme-ai`

#### OpenAI API Key

> Set your OpenAI API key as an environment variable.
> ```console
> # Using Linux or macOS
> $ export OPENAI_API_KEY=<your_api_key>
>
> # Using Windows
> $ set OPENAI_API=<your_api_key>
> ```

#### Google Vertex AI

> Set your Google Cloud project ID and location as environment variables.
> ```console
> $ export VERTEXAI_LOCATION=<your_location>
> $ export VERTEXAI_PROJECT=<your_project>
> ```

#### Using `pip`

> [![pip](https://img.shields.io/badge/PyPI-3775A9.svg?style=flat&logo=PyPI&logoColor=white)](https://pypi.org/project/readmeai/)
>
> ```sh
> readmeai --repository https://github.com/eli64s/readme-ai --api openai
> ```

#### Using `docker`

> [![docker](https://img.shields.io/badge/Docker-2496ED.svg?style=flat&logo=Docker&logoColor=white)](https://hub.docker.com/r/zeroxeli/readme-ai)
>
> ```sh
> docker run -it \
> -e OPENAI_API_KEY=$OPENAI_API_KEY \
> -v "$(pwd)":/app zeroxeli/readme-ai:latest \
> -r https://github.com/eli64s/readme-ai
> ```

#### Using `streamlit`

> [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://readme-ai.streamlit.app/)
>
> <sub>Try directly in your browser on <a href="https://streamlit.io/">Streamlit</a>, no installation required! For more details, check out the <a href="https://github.com/eli64s/readme-ai-streamlit">readme-ai-streamlit</a> repository.</sub>

<details closed>
<summary>
  <h4>From <code>source</code></h4>
</summary>

#### Using `bash`
>
> [![bash](https://img.shields.io/badge/GNU%20Bash-4EAA25.svg?style=flat&logo=GNU-Bash&logoColor=white)](https://www.gnu.org/software/bash/)
>
> ```console
> $ conda activate readmeai
> $ python3 -m readmeai.cli.commands -r https://github.com/eli64s/readme-ai
> ```

#### Using `poetry`
> [![Poetry](https://img.shields.io/endpoint?url=https://python-poetry.org/badge/v0.json)](https://python-poetry.org/)
>
> ```console
> $ poetry shell
> $ poetry run python3 -m readmeai.cli.commands -r https://github.com/eli64s/readme-ai
> ```

</details>

---

### 🧪 Tests

#### Using `pytest`
> [![pytest](https://img.shields.io/badge/Pytest-0A9EDC.svg?style=flat&logo=Pytest&logoColor=white)](https://docs.pytest.org/en/7.1.x/contents.html)
> ```console
> $ make pytest
> ```

#### Using `nox`
> ```console
> $ nox -f noxfile.py
> ```

> [!TIP]
>
> <sub>Use [nox](https://nox.thea.codes/en/stable/) to test application against multiple Python environments and dependencies!</sub>

---

## 🧩 Configuration

Run the `readmeai` command in your terminal with the following options to tailor your README file.

### CLI Options

| Option | Type | Description | Default Value  |
| ------ | ---- | ----------- | -------------- |
| `--align`, `-a` | String | Align the text in the README.md file's header. | `center` |
| `--api` | String | LLM API service to use for text generation. | `None` |
| `--badges`, `-b` | String | Badge icon style types for README.md badges. | [see below](https://github.com/eli64s/readme-ai?tab=readme-ov-file#badges) |
| `badge-color` | String | Badge color name or hex code. | `0080ff` |
| `--emojis`, `-e` | Boolean | Adds emojis to the README.md file's header sections. | `False` |
| `--image`, `-i` | String | Project logo image displayed in the README file header. | `blue` |
| `🚧 --language` | String | Language for generating the README.md file. | `en` |
| `--max-tokens` | Integer | Maximum context window of the LLM API.  | `3899` |
| `--model`, `-m` | String | LLM API to use for text generation. | `gpt-3.5-turbo` |
| `--output`, `-o` | String | Output file name for the README file. | `readme-ai.md` |
| `--repository`, `-r` | String | Repository URL or local directory path. | `None` |
| `--temperature`, `-t` | Float | Sets the creativity level for content generation. | `1.0` |
| `🚧 --template` | String | README template style. | `default` |
| `--tree-depth` | Integer | Maximum depth of the directory tree structure. | `3` |
| `--help` | | Displays help information about the command and its options. | |

<sub><em><code>🚧 feature currently under development</code></em>

---

### Badges

The `--badges` option lets you select the style of the default badge set.

<table>
  <tr>
    <th style="text-align: left;">Style</th>
    <th style="text-align: center;">Preview</th>
  </tr>
  <tr>
    <td><strong>default</strong></td>
    <td align="center"><a href="https://img.shields.io/github/license/eli64s/readme-ai?flat&color=0080ff&logo=opensourceinitiative&logoColor=white" target="_blank"><img src="https://img.shields.io/github/license/eli64s/readme-ai?flat&color=0080ff&logo=opensourceinitiative&logoColor=white"></a> <a href="https://img.shields.io/github/last-commit/eli64s/readme-ai?flat&color=0080ff&logo=git&logoColor=white" target="_blank"><img src="https://img.shields.io/github/last-commit/eli64s/readme-ai?flat&color=0080ff&logo=git&logoColor=white"></a> <a href="https://img.shields.io/github/languages/top/eli64s/readme-ai?flat&color=0080ff" target="_blank"><img src="https://img.shields.io/github/languages/top/eli64s/readme-ai?flat&color=0080ff"></a> <a href="https://img.shields.io/github/languages/count/eli64s/readme-ai?flat&color=0080ff" target="_blank"><img src="https://img.shields.io/github/languages/count/eli64s/readme-ai?flat&color=0080ff"></a></td>
  </tr>
  <tr>
    <td><strong>flat</strong></td>
    <td align="center"><a href="https://img.shields.io/badge/Python-3776AB.svg?&style=flat&logo=Python&logoColor=white" target="_blank"><img src="https://img.shields.io/badge/Python-3776AB.svg?&style=flat&logo=Python&logoColor=white"></a></td>
  </tr>
  <tr>
    <td><strong>flat-square</strong></td>
    <td align="center"><a href="https://img.shields.io/badge/Python-3776AB.svg?&style=flat-square&logo=Python&logoColor=white" target="_blank"><img src="https://img.shields.io/badge/Python-3776AB.svg?&style=flat-square&logo=Python&logoColor=white"></a></td>
  </tr>
  <tr>
    <td><strong>for-the-badge</strong></td>
    <td align="center"><a href="https://img.shields.io/badge/Python-3776AB.svg?&style=for-the-badge&logo=Python&logoColor=white" target="_blank"><img src="https://img.shields.io/badge/Python-3776AB.svg?&style=for-the-badge&logo=Python&logoColor=white"></a></td>
  </tr>
  <tr>
    <td><strong>plastic</strong></td>
    <td align="center"><a href="https://img.shields.io/badge/Python-3776AB.svg?&style=plastic&logo=Python&logoColor=white" target="_blank"><img src="https://img.shields.io/badge/Python-3776AB.svg?&style=plastic&logo=Python&logoColor=white"></a></td>
  </tr>
  <tr>
    <td><strong>skills</strong></td>
    <td align="center"><a href="https://skillicons.dev/" target="_blank"><img src="https://skillicons.dev/icons?i=py" alt="Python Skill Icon"></a></td>
  </tr>
  <tr>
    <td><strong>skills-light</strong></td>
    <td align="center"><a href="https://skillicons.dev/" target="_blank"><img src="https://skillicons.dev/icons?i=py&theme=light" alt="Python Skill Light Icon"></a></td>
  </tr>
  <tr>
    <td><strong>social</strong></td>
    <td align="center"><a href="https://img.shields.io/badge/Python-3776AB.svg?&style=social&logo=Python&logoColor=white" target="_blank"><img src="https://img.shields.io/badge/Python-3776AB.svg?&style=social&logo=Python&logoColor=white"></a></td>
  </tr>
</table>

When providing the `--badges` option, readme-ai does two things:

1. Formats the default badge set to match the selection (i.e. flat, flat-square, etc.).
2. Generates an additional badge set representing your projects dependencies and tech stack (i.e. Python, Docker, etc.)

#### Example
>
> ```console
> $ readmeai --badges flat-square --repository https://github.com/eli64s/readme-ai
> ```
>

#### Output
>
> {... project logo ...}
>
> {... project name ...}
>
> {...project slogan...}
>
> <img src="https://img.shields.io/github/license/eli64s/readme-ai?style=flat-square&color=0080ff&logo=opensourceinitiative&logoColor=white">
> <img src="https://img.shields.io/github/last-commit/eli64s/readme-ai?style=flat-square&color=0080ff&logo=git&logoColor=white">
> <img src="https://img.shields.io/github/languages/top/eli64s/readme-ai?style=flat-square&color=0080ff">
> <img src="https://img.shields.io/github/languages/count/eli64s/readme-ai?style=flat-square&color=0080ff">
>
> <br>
>
>	*Developed with the software and tools below.*
>
> <img src="https://img.shields.io/badge/GNU%20Bash-4EAA25.svg?style=flat-square&logo=GNU-Bash&logoColor=white">
> <img src="https://img.shields.io/badge/tqdm-FFC107.svg?style=flat-square&logo=tqdm&logoColor=black">
> <img src="https://img.shields.io/badge/Pydantic-E92063.svg?style=flat-square&logo=Pydantic&logoColor=white">
> <img src="https://img.shields.io/badge/YAML-CB171E.svg?style=flat-square&logo=YAML&logoColor=white" alt="YAML">
> <img src="https://img.shields.io/badge/Poetry-60A5FA.svg?style=flat-square&logo=Poetry&logoColor=white">
> <img src="https://img.shields.io/badge/OpenAI-412991.svg?style=flat-square&logo=OpenAI&logoColor=white">
> <br>
> <img src="https://img.shields.io/badge/Python-3776AB.svg?style=flat-square&logo=Python&logoColor=white">
> <img src="https://img.shields.io/badge/AIOHTTP-2C5BB4.svg?style=flat-square&logo=AIOHTTP&logoColor=white">
> <img src="https://img.shields.io/badge/Docker-2496ED.svg?style=flat-square&logo=Docker&logoColor=white">
> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF.svg?style=flat-square&logo=GitHub-Actions&logoColor=white">
> <img src="https://img.shields.io/badge/Pytest-0A9EDC.svg?style=flat-square&logo=Pytest&logoColor=white">
>
> <br>
>
> {... end of header ...}
>

---

### Project Logo

Select a project logo using the `--image` option. The following options are available:

<table>
  <tr>
    <td><strong>blue</strong></td>
    <td><strong>gradient</strong></td>
    <td><strong>black</strong></td>
  </tr>
  <tr>
    <td><img src="https://raw.githubusercontent.com/PKief/vscode-material-icon-theme/ec559a9f6bfd399b82bb44393651661b08aaf7ba/icons/folder-markdown-open.svg" width="100"></td>
    <td><img src="https://img.icons8.com/?size=512&id=55494&format=png" width="100"></td>
    <td><img src="https://img.icons8.com/external-tal-revivo-regular-tal-revivo/96/external-readme-is-a-easy-to-build-a-developer-hub-that-adapts-to-the-user-logo-regular-tal-revivo.png" width="100"></td>
  </tr>
  <tr>
    <td><strong>cloud</strong></td>
    <td><strong>purple</strong></td>
    <td><strong>grey</strong></td>
  </tr>
  <tr>
    <td><img src="https://cdn-icons-png.flaticon.com/512/6295/6295417.png" width="100"></td>
    <td><img src="https://img.icons8.com/external-tal-revivo-duo-tal-revivo/100/external-markdown-a-lightweight-markup-language-with-plain-text-formatting-syntax-logo-duo-tal-revivo.png" width="100"></td>
    <td><img src="https://img.icons8.com/external-tal-revivo-filled-tal-revivo/96/external-markdown-a-lightweight-markup-language-with-plain-text-formatting-syntax-logo-filled-tal-revivo.png" width="100"></td>
  </tr>
</table>

For custom images, see the following options:
* Use `--image file` option to invoke a prompt to upload a custom image file.
* Use `--image url` option to invoke a prompt to enter a custom image URL.
* Use `--image llm` option to generate a logo using an LLM API (in development).

---

## 🛠 Project Roadmap

- [ ] Add new CLI options to enhance README file customization.
  - [X] `--api` Integrate singular interface for all LLM APIs (OpenAI, Google Cloud, etc.)
  - [ ] `--audit` to review existing README files and suggest improvements.
  - [ ] `--template` to select a README template style (i.e. ai, data, web, etc.)
  - [ ] `--language` to generate README files in any language (i.e. zh-CN, ES, FR, JA, KO, RU)
- [ ] Develop robust documentation generator to build full project docs (i.e. Sphinx, MkDocs)
- [ ] Create community-driven templates for README files and gallery of readme-ai examples.
- [ ] GitHub Actions script to automatically update README file content on repository push.

---

## 📒 Changelog

[Changelog](https://github.com/eli64s/readme-ai/blob/main/CHANGELOG.md)

---

## 🤝 Contributing

- [Discussions](https://github.com/eli64s/readme-ai/discussions)
- [Open an Issue](https://github.com/eli64s/readme-ai/issues)
- [Contributing Guidelines](https://github.com/eli64s/readme-ai/blob/main/CONTRIBUTING.md)

---

## 📄 License

[MIT](https://github.com/eli64s/readme-ai/blob/main/LICENSE)

---

## 👏 Acknowledgments

*Badges*
  - [Shields.io](https://shields.io/)
  - [Aveek-Saha/GitHub-Profile-Badges](https://github.com/Aveek-Saha/GitHub-Profile-Badges)
  - [Ileriayo/Markdown-Badges](https://github.com/Ileriayo/markdown-badges)
  - [tandpfun/skill-icons](https://github.com/tandpfun/skill-icons)


<p align="right">
  <a href="#-overview"><b>Return</b></a>
</p>

---
