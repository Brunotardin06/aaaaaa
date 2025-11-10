![AnnotAISE logo](frontend/public/Full_Logo_DarkMode.svg)

## Descrição do Projeto

O **AnnotAISE** é uma plataforma de rotulação orientada por **CSV** com dois perfis:

- **Pesquisador(a):** cria **modelos de rotulação** a partir de um CSV. Cada **coluna** vira um **contexto**; no **construtor** adiciona **seções** e **perguntas** (ex.: texto, número, faixa, múltipla escolha, booleano), podendo marcar como **obrigatórias**. Ao finalizar, o sistema gera **N formulários** para **N linhas** do CSV.
- **Usuário comum (anotador):** acessa as rotulações atribuídas, **responde os formulários** e **submete** as respostas.

## Who this project is for

This project is intended for:

- **Researchers / data teams** who want to quickly create CSV-driven labeling templates (map columns to contexts, add questions, generate one form per row) and manage progress/export results.
- **Annotators (end users)** who need a simple interface to access assigned labelings, answer forms, and submit responses.

## Project dependencies

Before using **AnnotAISE**, ensure you have the following prerequisites installed:

- **Python 3.12+** — required for running the Django backend.  
- **Node.js 20+** — required for the Next.js frontend.  
- **PostgreSQL 14+** — database used by the backend.  
- **Docker and Docker Compose v2** *(recommended)* — to run all services easily in containers.  
- **Git** — to clone and manage the project repository.

---

### 1. Docker Desktop
- **Windows**:
  1. Download [Docker Desktop for Windows](https://docs.docker.com/desktop/install/windows-install/)
  2. Run the installer
  3. If prompted, enable WSL 2 (Windows Subsystem for Linux)
  4. Restart your computer after installation
  5. Verify the installation by opening terminal and typing: `docker --version`

- **macOS**:
  1. Download [Docker Desktop for Mac](https://docs.docker.com/desktop/install/mac-install/)
  2. Drag Docker to Applications folder
  3. Open Docker and allow installation of additional components
  4. Verify the installation by opening terminal and typing: `docker --version`

- **Linux (Ubuntu)**:
  ```bash
  sudo apt update
  sudo apt install docker.io
  sudo systemctl start docker
  sudo systemctl enable docker
  sudo usermod -aG docker $USER
  # Logout and login again
  docker --version
  ```

### 2. Docker Compose
- **Windows/macOS**: 
  - Already included in Docker Desktop

- **Linux**:
  ```bash
  sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  sudo chmod +x /usr/local/bin/docker-compose
  docker-compose --version
  ```

docker compose version

### Verificar Git
git --version
### 3. Git
- **Windows**:
  1. Download [Git for Windows](https://git-scm.com/download/win)
  2. Run the installer
  3. Keep default options during installation
  4. Verify installation: `git --version`

- **macOS**:
  ```bash
  brew install git
  git --version
  ```

- **Linux (Ubuntu)**:
  ```bash
  sudo apt update
  sudo apt install git
  git --version
  ```
