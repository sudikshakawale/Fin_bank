
<img width="959" height="473" alt="Screenshot 2026-06-20 025019" src="https://github.com/user-attachments/assets/9cc2609e-e243-41f2-800e-5d3bcfe035de" />

<img width="959" height="479" alt="Screenshot 2026-06-20 025027" src="https://github.com/user-attachments/assets/54edc15e-96ee-4647-aee1-59ba3c30de41" />
<img width="958" height="436" alt="Screenshot 2026-06-30 102055" src="https://github.com/user-attachments/assets/a5fc4b59-d925-495b-8d95-f3fc3050cd3c" />
<img width="956" height="434" alt="Screenshot 2026-06-30 102212" src="https://github.com/user-attachments/assets/d020e140-1ee3-4565-a923-994dc5e5bb72" />

<img width="329" height="230" alt="Screenshot 2026-06-30 102825" src="https://github.com/user-attachments/assets/57509cb2-bb50-41f2-be6c-ad3a02bd2467" />

<img width="252" height="223" alt="Screenshot 2026-06-30 102750" src="https://github.com/user-attachments/assets/688bc47c-7835-49a2-a866-acc8c482fc05" />

<img width="341" height="259" alt="Screenshot 2026-06-30 102601" src="https://github.com/user-attachments/assets/c82445a9-43cf-4360-be97-f1c80fec2023" />

<img width="702" height="421" alt="Screenshot 2026-06-20 101150" src="https://github.com/user-attachments/assets/e452e14f-2cc4-4308-899e-ea9ca433a245" />

<img width="366" height="125" alt="Screenshot 2026-06-30 102708" src="https://github.com/user-attachments/assets/b48b83d1-e571-45ff-95f9-88b68d3448e2" />





<img width="959" height="469" alt="Screenshot 2026-06-20 025042" src="https://github.com/user-attachments/assets/4fe21e91-4eb8-41b0-9753-4015c4efb6ed" />



<img width="1916" height="1074" alt="image" src="https://github.com/user-attachments/assets/d5c5ec91-eb0a-4c5c-ae4c-01c15a6125f8" />

<img width="1919" height="1020" alt="Screenshot 2026-05-23 020226" src="https://github.com/user-attachments/assets/5a74e04f-d6ae-48f0-9806-70fc57e3d2b4" />

<img width="1915" height="942" alt="Screenshot 2026-05-23 014938" src="https://github.com/user-attachments/assets/03cd9188-3a1a-4710-a4d6-fde09367db48" />
<img width="1919" height="1020" alt="Screenshot 2026-05-23 014817" src="https://github.com/user-attachments/assets/f8a34b2c-60ef-4a80-a54d-b38e60182f24" />
<img width="1919" height="988" alt="Screenshot 2026-05-23 000140" src="https://github.com/user-attachments/assets/044dee2c-3eeb-427f-80ac-bb6602a5095d" />
<img width="1919" height="959" alt="Screenshot 2026-05-23 000130" src="https://github.com/user-attachments/assets/a01e2299-e26c-481d-8a4a-28f72b035eba" />



# Online Banking System V2.0.2

This is an Online Banking Concept created using Django Web Framework.


## Features

* Create Bank Account.
* Deposit & Withdraw Money
* Bank Account Type Support (e.g. Current Account, Savings Account)
* Interest calculation depending on the Bank Account type
* Transaction report with a date range filter 
* See balance after every transaction in the Transaction Report
* Calculate Monthly Interest Using Celery Scheduled tasks
* More efficient and accurate interest calculation and balance update
* Ability to add Minimum and Maximum Transaction amount restriction
* Modern UI with Tailwind CSS


## Prerequisites

Be sure you have the following installed on your development machine:

+ Python >= 3.7
+ Redis Server
+ Git
+ pip
+ Virtualenv (virtualenvwrapper is recommended)

## Requirements

+ celery==4.4.7
+ Django==3.2
+ django-celery-beat==2.0.0
+ python-dateutil==2.8.1
+ redis==3.5.3

## Install Redis Server

[Redis Quick Start](https://redis.io/topics/quickstart)

Run Redis server
```bash
redis-server
```

## Project Installation

To setup a local development environment:

Create a virtual environment in which to install Python pip packages. With [virtualenv](https://pypi.python.org/pypi/virtualenv),
```bash
virtualenv venv            # create a virtualenv
source venv/bin/activate   # activate the Python virtualenv 
```

or with [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/),
```bash
mkvirtualenv -p python3 {{project_name}}   # create and activate environment
workon {{project_name}}   # reactivate existing environment
```

Clone GitHub Project,
```bash
git@github.com:saadmk11/banking-system.git

cd banking-system
```

Install development dependencies,
```bash
pip install -r requirements.txt
```

Migrate Database,
```bash
python manage.py migrate
```

Run the web application locally,
```bash
python manage.py runserver # 127.0.0.1:8000
```

Create Superuser,
```bash
python manage.py createsuperuser
```

Run Celery
(Different Terminal Window with Virtual Environment Activated)
```bash
celery -A banking_system worker -l info

celery -A banking_system beat -l info
```
