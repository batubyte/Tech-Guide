# Python Guide & useful codes

## 1. Install Visual Studio Code
- **[Download VSCode](https://code.visualstudio.com/Download)**

## 2. File structure
    project/
    │
    ├── README.md
    ├── LICENSE
    ├── requirements.txt
    ├── .env
    ├── src/
    │   ├── server.py
    │   └── client.py
    └── tests/
        ├── test_1.py
        └── test_2.py
## 3. Linux Virtual envrionment setup
```sh
python3 -m venv venv
source venv/bin/activate
python main.py
pip freeze > requirements.txt # Make requirements
pip install -r requirements.txt # Install requirements
deactivate
```

## 4. Windows virtual envrionment setup
```bat
python -m venv venv
venv\Scripts\activate
python main.py
pip freeze > requirements.txt
pip install -r requirements.txt
deactivate
```

## 5. Code
```py
import ...

def main():
    ...

if __name__ == '__main__':
    main()
```

## 6. Get current script path
```py
import sys, os
def get_current_script_path():
    if getattr(sys, 'frozen', False):
        return os.path.dirname(sys.executable)
    else:
        return os.path.dirname(os.path.realpath(__file__))
```
