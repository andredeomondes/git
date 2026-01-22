# 🚀 Guia Definitivo de Git & GitHub | Ultimate Git & GitHub Guide

![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

---

## 🇧🇷 Português

### 🧠 Conceitos Fundamentais
O Git é um sistema de controle de versão distribuído. Ele gerencia o histórico de alterações através de 3 estados principais:
1. **Working Directory:** Sua pasta local onde os arquivos são editados.
2. **Staging Area (Index):** A zona de preparação para o próximo commit.
3. **Local Repository:** Onde o Git armazena as versões (commits) permanentemente no seu PC.

### 🛠️ Comandos de Sobrevivência (Essenciais)
* `git init`: Inicia um repositório na pasta atual.
* `git status`: O "GPS" do desenvolvedor. Mostra o estado dos arquivos.
* `git add <arquivo>`: Move arquivos específicos para a Staging Area.
* `git add .`: Move **todos** os arquivos alterados para a Staging Area.
* `git commit -m "mensagem"`: Cria um ponto na história com uma descrição.
* `git commit -a -m "msg"`: Atalho que pula o `git add` (apenas para arquivos já rastreados).
* `git log --oneline --graph --all`: Visualiza o histórico de forma gráfica e resumida.

### 🌿 Ramificação e Colaboração (Branches)
* `git checkout -b <nome>`: Cria uma nova branch e alterna para ela.
* `git switch <nome>`: Forma moderna de alternar entre branches.
* `git merge <nome>`: Une o histórico da branch citada à sua branch atual.
* `git branch -d <nome>`: Deleta uma branch que já foi mesclada.

### 🌍 Sincronização Remota
* `git remote add origin <url>`: Conecta seu PC ao repositório no GitHub.
* `git push -u origin <branch>`: Envia seus commits e define o destino padrão.
* `git pull origin <branch>`: Baixa as novidades do servidor e mescla no seu código.
* `git fetch`: Baixa as novidades do servidor **sem** alterar seu código local.

### ⚖️ Tabela: Merge vs. Rebase
| Característica | Git Merge | Git Rebase |
| :--- | :--- | :--- |
| **Histórico** | Não linear (preserva ramos) | Linear (histórico limpo/reto) |
| **Uso comum** | Unir código de equipes | Limpar histórico antes do PR |
| **Conflitos** | Resolvidos uma única vez | Resolvidos commit por commit |

### 💡 Fluxo de Trabalho Recomendado (Best Practices)
```bash
# 1. Comece o dia atualizando o código
git pull origin main

# 2. Crie uma branch específica para sua tarefa
git checkout -b feat/nova-funcionalidade

# 3. Durante o desenvolvimento (salve seu progresso)
git add .
git commit -m "feat: implementa lógica de login"

# 4. Antes de enviar, verifique se houve mudanças na main
git checkout main
git pull origin main
git checkout feat/nova-funcionalidade
git rebase main

# 5. Envie para o servidor
git push origin feat/nova-funcionalidade
```
--- 
## 🇺🇸 English
![Git](https://img.shields.io/badge/git-%23F05033.svg?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

---

## 🧠 Core Concepts
Git is a **distributed version control system**. Unlike centralized systems, every developer has a full copy of the project history on their machine.

### The 3 Git Stages
1. **Working Directory:** Where you are currently editing your files.
2. **Staging Area (Index):** The "waiting room" for changes before they are committed.
3. **Local Repository:** Where Git permanently stores the snapshots (commits) of your project.

---

## 🛠️ Essential Command Toolkit

### 📂 Navigation & Initialization
* `cd [path]`: Navigate to a specific folder.
* `clear`: Clear the terminal screen.
* `git init`: Initialize a new Git repository in the current folder.
* `git status`: The most important command. Shows the state of your files.

### 📝 Tracking & Committing
* `git add <file>`: Move a specific file to the Staging Area.
* `git add .`: Move **all** modified files to the Staging Area.
* `git commit -m "message"`: Permanently record your changes in the local repository.
* `git commit -a -m "message"`: Shortcut to add and commit tracked files in one step.
* `.gitignore`: A file to list everything Git should ignore (e.g., `node_modules`, `.env`).

### 🔍 Inspection & Diffs
* `git diff`: Shows changes in the working directory that are not yet staged.
* `git diff --staged`: Shows what is in the Staging Area ready to be committed.
* `git log`: Shows the full commit history.
* `git log -p`: Shows the history with detailed line-by-line changes (patches).
* `git log --oneline --graph --all`: A visual, summarized tree of all branches.

---

## 🌿 Branching & Collaboration
* `git branch`: Lists all local branches.
* `git checkout -b <name>`: Creates a new branch and switches to it immediately.
* `git switch <name>`: Modern command to switch between existing branches.
* `git merge <name>`: Combines the history of the specified branch into your current one.

### 🌍 Remote Syncing
* `git remote add origin <url>`: Links your local repository to a remote server (GitHub).
* `git clone <url>`: Downloads an entire project and its history to your PC.
* `git pull origin <branch>`: Fetches updates from the server and merges them locally.
* `git push origin <branch>`: Sends your local commits to the remote server.

---

## ⚖️ Merge vs. Rebase: Comparison

| Feature | **Git Merge** | **Git Rebase** |
| :--- | :--- | :--- |
| **History** | Preserves actual chronology (Non-linear) | Creates a clean, straight line (Linear) |
| **Traceability** | Creates a "Merge Commit" | No extra commits (Cleaner log) |
| **Conflicts** | Resolved once during the merge | Resolved commit by commit |
| **Best For** | Shared branches / Team features | Private local branches / Polishing history |

---

## 💡 Recommended Professional Workflow
Follow these steps for a clean and efficient development cycle:

```bash
# 1. Start by updating your main branch
git checkout main
git pull origin main

# 2. Create a specific branch for your task
git checkout -b feat/new-feature-name

# 3. Work and save your progress frequently
git add .
git commit -m "feat: implement specific logic"

# 4. Stay updated with the team (avoiding big conflicts later)
git fetch origin
git rebase origin/main

# 5. Push your work and open a Pull Request
git push origin feat/new-feature-name
```
