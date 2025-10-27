# 🎓 Masters of Science in Applied Data Science - University of San Diego

This repository is a resource hub that I used to collect information that I found helpful while in the MS-ADS program at the University of San Diego. I hope this could also be useful for others who are taking the program.

This repository includes setup guides, environment configuration notes, and course references that I found useful throught the program.

## 💻 VS Code and Windows Development

I used to do development on a Mac but have since replaced my main PCs with Windows-based computers. For the most part, the MSADS program can be done in Windows. In a couple of classes, it's necessary to run _Python_ and _R_ in the same Jupyter Notebook. Unfortunately, this can't be done natively in Windows. Thankfully, Windows Subsystem for Linux 2 (WSL2) makes this possible.

- [Setting up WSL2 and VSCode in Windows](setup/vscode_and_wsl2.md)
- [Creating a Conda environment to run Python and R in Windows](setup/python_r_windows.md)
- [Export Jupyter Notebooks as PDF from VSCode](setup/jnotebook_export_pdf.md)
- [Using Aliases in WSL2](setup/wsl2_aliases.md)
- [Creating and Updating Conda Environments from YAML file](setup/creating_conda_envs.md)

## Courses

Spring 2024

- ADS 500A - Probability and Statistics for Data Science
- ADS 500B - Data Science Programming

Summer 2024

- ADS 501 - Foundations of Data Science and Data Ethics
- ADS 502 - Applied Data Mining

Fall 2024

- ADS 505 - Applied Data Science for Business
- ADS 506 - Applied Time Series Analysis

Spring 2025

- ADS 507 - Practical Data Engineering
- ADS 508 - Data Science with Cloud Computing

Summer 2025

- ADS 503 - Applied Predictive Modeling
- ADS 504 - Machine Learning and Deep Learning for Data Science

Fall 2025

- ADS 509 - Applied Text Mining
- ADS 599 - Capstone Project

## Custom EDA Library

I started developing my own EDA library since there is a lot of repetitive code when it comes to exploratory data analysis. You can find it here if you want to check it out. Just be aware that it is in active development and it might be a long time between library updates.

You can find that library here: [jcds repository](https://github.com/junclemente/jcds).

This will make the functions useable in the notebook.
