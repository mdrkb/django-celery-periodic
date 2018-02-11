# mycelery
Django periodic task example using Celery and RabbitMQ.

## Getting Started

### Prerequisities
* Python >= 3.5.2
* RabbitMQ
* Virtualenv

### Installing
```
git clone https://github.com/mdrkb/django-celery-periodic.git
cd django-celery-periodic
virtualenv venv
source venv/bin/activate
pip install -r requirements.txt
cd mycelery
python manage.py migrate
```

### Running Django Server
```
python manage.py runserver
```

### Running RabbitMQ Worker and Beat
Open another terminal. Navigate inside ```../mycelery/mycelery/``` by activating virutal environment. Then run the following command:
```
celery -A mycelery worker -l info -B
```

