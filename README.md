
<img width="959" height="473" alt="Screenshot 2026-06-20 025019" src="https://github.com/user-attachments/assets/9cc2609e-e243-41f2-800e-5d3bcfe035de" />

<img width="956" height="371" alt="image" src="https://github.com/user-attachments/assets/c9afe0dd-35c4-412d-8e48-4bf0eb923a8f" />

<img width="959" height="479" alt="Screenshot 2026-06-20 025027" src="https://github.com/user-attachments/assets/54edc15e-96ee-4647-aee1-59ba3c30de41" />

<img width="820" height="305" alt="image" src="https://github.com/user-attachments/assets/a42c1d99-612f-41fc-80ed-a3fd87aaa413" />

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


<img width="959" height="417" alt="image" src="https://github.com/user-attachments/assets/f869ae43-0798-4251-a2a7-e190ac77f786" />

<img width="959" height="350" alt="image" src="https://github.com/user-attachments/assets/5bf76381-3806-4e8d-b6b9-7f29ba405068" />

<img width="240" height="368" alt="image" src="https://github.com/user-attachments/assets/dc606264-f7da-4904-a0be-c083678c3974" />



<img width="820" height="305" alt="image" src="https://github.com/user-attachments/assets/dd1bdf9b-fcdc-478d-a1f6-d105bdd4000a" />

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
