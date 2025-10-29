# 🎓 Master of Science in Applied Data Science — University of San Diego

This repository serves as a resource hub where I’ve collected information, notes, and configurations that I found helpful during the **Master of Science in Applied Data Science (MS-ADS)** program at the **University of San Diego**. I hope this can also be useful for others currently enrolled in — or preparing to start — the program.

It includes setup guides, environment configuration notes, and course references that I found most useful throughout my studies.

> 🧠 **Note:** Some setup guides in this repository were refined or reformatted with the help of ChatGPT to improve clarity and organization. All technical content is based on my actual configurations and experiences during the program.

---

## 📖 Table of Contents

- [🎓 Master of Science in Applied Data Science — University of San Diego](#-master-of-science-in-applied-data-science--university-of-san-diego)
  - [📖 Table of Contents](#-table-of-contents)
  - [💻 VS Code and Windows Development](#-vs-code-and-windows-development)
  - [📚 Courses](#-courses)
    - [Spring 2024](#spring-2024)
    - [Summer 2024](#summer-2024)
    - [Fall 2024](#fall-2024)
    - [Spring 2025](#spring-2025)
    - [Summer 2025](#summer-2025)
    - [Fall 2025](#fall-2025)
  - [🧩 Custom EDA Library](#-custom-eda-library)
  - [📰 License](#-license)

---

## 💻 VS Code and Windows Development

I used to develop primarily on a Mac but have since replaced my main PCs with Windows-based systems. For the most part, the MS-ADS program can be completed entirely in Windows.  

However, in a few classes it’s necessary to run both _Python_ and _R_ in the same Jupyter Notebook — something that isn’t supported natively in Windows. Thankfully, **Windows Subsystem for Linux 2 (WSL2)** makes this possible.

Setup guides and references:

- [Setting up WSL2 and VS Code in Windows](setup/vscode_and_wsl2.md)
- [Creating a Conda Environment to Run Python and R in Windows](setup/python_r_windows.md)
- [Exporting Jupyter Notebooks as PDF from VS Code](setup/jnotebook_export_pdf.md)
- [Using Aliases in WSL2](setup/wsl2_aliases.md)
- [Creating and Updating Conda Environments from a YAML File](setup/creating_conda_envs.md)
- [Recommended VS Code Extensions for MS-ADS](setup/vscode_extensions.md)

---

## 📚 Courses

### Spring 2024
- ADS 500A — Probability and Statistics for Data Science  
- ADS 500B — Data Science Programming  

### Summer 2024
- ADS 501 — Foundations of Data Science and Data Ethics  
- ADS 502 — Applied Data Mining  

### Fall 2024
- ADS 505 — Applied Data Science for Business  
- ADS 506 — Applied Time Series Analysis  

### Spring 2025
- ADS 507 — Practical Data Engineering  
- ADS 508 — Data Science with Cloud Computing  

### Summer 2025
- ADS 503 — Applied Predictive Modeling  
- ADS 504 — Machine Learning and Deep Learning for Data Science  

### Fall 2025
- ADS 509 — Applied Text Mining  
- ADS 599 — Capstone Project  

---

## 🧩 Custom EDA Library

I began developing my own **Exploratory Data Analysis (EDA)** library to simplify repetitive EDA tasks that come up across multiple courses.  
It’s still in active development, so updates may be infrequent, but it’s already functional for common EDA workflows.

You can check it out here:  
👉 [**jcds repository**](https://github.com/junclemente/jcds)

Once installed, the library’s functions can be imported directly for use within Jupyter Notebooks.

---

## 📰 License

[MIT License](./LICENSE)

Copyright (c) 2025 Jun Clemente

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
