# ✦ Installation av Virtuella Miljöer och Shellkommandon (Python) ✦

När du arbetar med virtuella miljöer i Python skiljer sig kommandona beroende på operativsystem och terminal (shell), främst på grund av hur aktivering av miljön och sökvägen till `.venv/bin/` eller `.venv/Scripts/` hanteras.

---

## 🔹 1. macOS & Linux (Bash/Zsh i t.ex. VS Code)

```Shell
# Ta bort eventuell gammal miljö
rm -rf .venv

# Skapa ny virtuell miljö 
python3 -m venv .venv 

# Aktivera miljön
source .venv/bin/activate

# Uppgradera pip
pip install --upgrade pip

# Installera beroenden
pip install -r requirements.txt

# Avaktivera miljön 
deactivate

```

## 🔹 2. Windows (Bash/Zsh i t.ex. VS Code om WSL är intstallerat)

```Shell

# kolla om du har WSL installerat 

uname -a 

# Får du Microsoft från terminalen har du WSL installera enligt punkt 🔹 1.

```

## 🔹 3. Windows (Git Bash,Bash /Zsh i t.ex. VS Code utan WSL )

```Shell
# Ta bort eventuell gammal miljö
rm -rf .venv

# Skapa ny virtuell miljö 
python -m venv .venv

# OBS! Följande kommando fungerar INTE i Git Bash/Zsh på Windows rekommenderas byta till Powershell eller CMD terminal om du ska aktivera din virtuella miljö:
source .venv/Scripts/activate

# Uppgradera pip
pip install --upgrade pip

# Installera beroenden
pip install -r requirements.txt

# Avaktivera miljön 

deactivate

```

## 🔹 4. Windows PowerShell

```Shell 

# Ta bort eventuell gammal miljö
Remove-Item .venv -Recurse -Force

# Skapa ny virtuell miljö 
python -m venv .venv

# Aktivera miljön 
.venv\Scripts\Activate.ps1

# Uppgradera pip
pip install --upgrade pip

# Installera beroenden
pip install -r requirements.txt

# Avaktivera miljön 

deactivate

```

## 🔹 5. Windows CMD

```Shell

# Ta bort eventuell gammal miljö
rmdir /s /q .venv

# Skapa ny virtuell miljö 
python -m venv .venv

# Aktivera miljön 
.venv\Scripts\Activate.bat

# Uppgradera pip
pip install --upgrade pip

# Installera beroenden
pip install -r requirements.txt

# Avaktivera miljön 

deactivate

```

## 🔹 6. Skapa en requirement fil 

```shell 

# Efter att ha aktiverat miljön installera valfritt paket

pip install Pytest

# Lista aktuella Python-paket i venv miljön

pip freeze 

# Skapa en requirement fil med aktuella Python-paket 

pip freeze > requirements.txt

```

## 🔹 7. Kolla om du kan använda Python eller Python 3 

```Shell

# kolla din version av Python

which python3 # MacOS/Linux

where python # Windows 

'''Får du Python 3 svar använd Python 3 annars använd Python. 
På vissa versioner av MacOS pekar Python mot Python 2 
'''

```
