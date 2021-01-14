# Python Virtual Environment Commands

### Create new environment in current folder
python3 -m venv venv

### Activate virtual environment
source venv/bin/activate

### Deactivate [...]
deactivate

### Export python package installation file
pip3 freeze > requirements.txt

### Install requirements.txt packages
pip3 install -r requirements.txt
