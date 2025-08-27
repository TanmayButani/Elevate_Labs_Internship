# 🔐 Password Strength Analyzer with Custom Wordlist Generator  

This project is part of my Cyber Security Internship. It demonstrates how to evaluate password strength using the `zxcvbn` library and generate custom wordlists from user inputs such as names, years, or pet names. The goal is to highlight weaknesses in predictable passwords and show how attackers may exploit them using wordlists.  

## 📌 Features  
- Analyze password strength (score, guesses, crack time, feedback)  
- Generate custom wordlists using personal details  
- Variations include leetspeak, numbers, symbols, and combinations  
- Export results to `.txt` format for cracking tools  
- Works in both CLI (Command Line Interface) and GUI (Tkinter)  

## 🛠 Tools & Libraries Used  
- Python 3.x  
- argparse – for CLI options  
- zxcvbn – for password strength analysis  
- NLTK – for word operations  
- Tkinter – for GUI interface  

## ⚙️ Installation & Setup  
- Clone the repository and move into the project folder  
- Create and activate a virtual environment
  ```bash
  python -m venv .venv
  .venv\Scripts\activate.bat
  ```
- Install the required libraries from `requirements.txt`
  ```bash
  python.exe -m pip install --upgrade pip
  pip install -r requirements.txt
  ```    

## 🚀 Usage  

### CLI Mode  
Run the analyzer by entering a password in the terminal to get a strength report.  
You will see details like score, estimated guesses, crack time, and feedback.  

![Analyzer](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/CLI_PWD_Analyzer.PNG) 

You can also generate a custom wordlist by entering personal inputs such as a name, year, or pet name. A `.txt` file will be created with variations of these inputs.  

![Generator](https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/CLI_PWD_Generator.PNG)

<p align="center">
  <img src="https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/CLI_PWD_Generator_Output.PNG" alt="GUI main window" width="600"/>
</p>

### GUI Mode  
You can also launch the Tkinter-based GUI tool.  
- Enter a password and click **Check Strength** to view score, crack time, and feedback.  
- Enter personal inputs and click **Generate Wordlist** to create and save a `.txt` wordlist.  

**GUI main window :** 
<p align="center">
  <img src="https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/GUI_1.PNG" alt="GUI main window" width="600"/>
</p>

GUI password strength check : 

<p align="center">
  <img src="https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/GUI_2.PNG" alt="GUI main window" width="600"/>
</p>

GUI wordlist generator save dialog :

<p align="center">
  <img src="https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/GUI_3.PNG" alt="GUI main window" width="600"/>
</p>

Saved WordList :

<p align="center">
  <img src="https://github.com/TanmayButani/Elevate_Labs_Internship/blob/main/Project/GUI_Result.PNG" alt="GUI main window" width="600"/>
</p>

## 📊 Deliverables  
- `password_analyzer.py` – CLI tool  
- `password_gui.py` – GUI tool  
- `requirements.txt` – Dependencies  
- `custom_wordlist.txt` – Example generated wordlist  
- `Password_Strength_Analyzer_Report.pdf` – Internship report  
- `README.md` – Documentation  

## 💡 Learning Outcomes  
Through this project I learned how to analyze password entropy using zxcvbn, how weak passwords can be exploited using wordlists, how to generate attack-specific wordlists from user details, and how to build both CLI and GUI tools in Python for cybersecurity tasks.  

## 📎 Screenshots to Include  
- Setup showing dependencies installed  
- CLI password analysis result  
- Generated wordlist file  
- GUI main window  
- GUI password strength check result  
- GUI wordlist generator save dialog  

