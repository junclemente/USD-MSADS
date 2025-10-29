# 🧩 Recommended VS Code Extensions for USD MS-ADS

Below is a curated list of Visual Studio Code extensions that I found useful throughout the **University of San Diego’s MS-ADS program**.  
All links go directly to the Visual Studio Code Marketplace so you can pick and choose what fits your workflow.  

> 💡 *ChatGPT was used to help format and organize this list, but the recommendations are based on my actual extensions list and experience during the program.*

---

## 🐍 Core Python
Essential tools for Python development, formatting, linting, and debugging.

- [**Python**](https://marketplace.visualstudio.com/items?itemName=ms-python.python) — Core Python language support, interactive Jupyter notebooks, and environment management.
- [**Pylance**](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance) — Fast, feature-rich language server for Python (type checking, autocomplete, IntelliSense).
- [**Black Formatter**](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter) — Code formatter that enforces consistent style using the *Black* standard.  
  - A lot of professors recommend using Black.
- [**isort**](https://marketplace.visualstudio.com/items?itemName=ms-python.isort) — Automatically sorts and organizes Python imports.
- [**Debugpy**](https://marketplace.visualstudio.com/items?itemName=ms-python.debugpy) — Python debugger used by VS Code’s “Run and Debug” feature.
- [**Python Environments**](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-python-envs) — Lets you easily select and manage Python interpreters and virtual environments.

---

## 📓 Notebooks & Data Wrangling
Extensions that enhance working with Jupyter notebooks and data exploration.

- [**Jupyter**](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter) — Full notebook integration inside VS Code.
- [**Data Wrangler**](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.datawrangler) — Spreadsheet-like data preview, transformation, and cleaning powered by Pandas.
- [**Jupytext**](https://marketplace.visualstudio.com/items?itemName=congyiwu.vscode-jupytext) — Syncs Jupyter notebooks with plain text files (`.py`, `.qmd`, or `.md`) for version control.

---

## 📊 R Language Support (ADS-503 / ADS-504)
Add-ons for running and editing R code and RMarkdown documents.

- [**R**](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r) — Provides syntax highlighting, IntelliSense, and integrated R terminal support.
- [**R Syntax**](https://marketplace.visualstudio.com/items?itemName=REditorSupport.r-syntax) — Adds detailed R language grammar and code coloring.
- [**RMarkdown**](https://marketplace.visualstudio.com/items?itemName=tianyishi.rmarkdown) — Enables `.Rmd` document editing and preview support.

---

## 💾 SQL & Data Access
For querying and viewing databases locally or remotely.

- [**SQLTools**](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools) — Database client for connecting to MySQL, PostgreSQL, SQLite, etc.
- [**SQLite Viewer**](https://marketplace.visualstudio.com/items?itemName=qwtel.sqlite-viewer) — Lightweight viewer for exploring `.db` and `.sqlite` files.

---

## 🧮 Documentation, Reports, and Markdown
Tools for writing reports, documentation, or Quarto projects.

- [**Quarto**](https://marketplace.visualstudio.com/items?itemName=quarto.quarto) — Supports Quarto notebooks (`.qmd`) for reproducible data science reports.
- [**Markdown All in One**](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one) — Enhanced Markdown editing with shortcuts and live preview.
- [**Markdownlint**](https://marketplace.visualstudio.com/items?itemName=davidanson.vscode-markdownlint) — Lints Markdown documents for style consistency and syntax issues.
- [**Markdown Table Prettify**](https://marketplace.visualstudio.com/items?itemName=darkriszty.markdown-table-prettify) — Automatically formats Markdown tables.

---

## ⚙️ Quality of Life
General utilities that improve workflow and productivity.

- [**dotenv**](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv) — Syntax highlighting for `.env` environment variable files.
- [**Path Intellisense**](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) — Auto-completes filenames and paths.
- [**Code Spell Checker**](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) — Detects spelling mistakes in comments, strings, and Markdown.

---

## 🤖 AI Coding Assistants
Optional AI pair programming and chat features.

> 💬 I run a server that I remote-SSH into with VS Code and use a local Ollama model via the **Continue** extension instead of paying for Copilot.  
> However, Copilot is *excellent*—especially for generating informative commit messages.

- [**Continue**](https://marketplace.visualstudio.com/items?itemName=Continue.continue) — Open-source AI coding assistant that integrates with models like GPT, Claude, and local LLMs directly inside VS Code. Provides inline suggestions, completions, and a side-panel chat for code reasoning.
- [**GitHub Copilot**](https://marketplace.visualstudio.com/items?itemName=github.copilot) — Context-aware AI code suggestions directly in the editor.
- [**GitHub Copilot Chat**](https://marketplace.visualstudio.com/items?itemName=github.copilot-chat) — Chat interface for asking questions, explaining code, and generating examples.

---

## 🎨 Theme & Icons
Customize the look and feel of your VS Code environment. I prefer coding in dark mode!

- [**Monokai Pro**](https://marketplace.visualstudio.com/items?itemName=monokai.theme-monokai-pro-vscode) — A refined, professional take on the classic Monokai theme with multiple variants.  
  - This is a paid extension with a free trial. It’s my personal favorite theme and worth the cost IMO
- [**Draculat At Night**](https://marketplace.visualstudio.com/items?itemName=bceskavich.theme-dracula-at-night) - A Dracula fork, with a darker flavor. 
- [**VSCode Icons**](https://marketplace.visualstudio.com/items?itemName=vscode-icons-team.vscode-icons) — Rich icon pack for better visual file recognition.
- [**:emojisense:**](https://marketplace.visualstudio.com/items?itemName=bierner.emojisense) — Emoji autocomplete and suggestions while typing.  
---

## 🧠 Installation Tip

When connected to a remote server via VS Code Remote-SSH,  
install extensions directly on the remote host using:

```bash
code --install-extension <extension-id>
```

