# HallowDjangoVue

## Clone Repository
```
git clone --recursive https://github.com/Ky7az/HallowDjangoVue
```

## Create Environment Files
Create *.env* file here
```
POSTGRES_USER=your_db_user
POSTGRES_PASSWORD=your_db_password
POSTGRES_DB=your_db_name
```

Create *.env* file into *DjangoHallow*
```
DEBUG=False
SECRET_KEY=your_secret_key
ALLOWED_HOSTS=your_domain_name
DB_ENGINE=django.db.backends.postgresql
DB_DATABASE=your_db_name
DB_USER=your_db_user
DB_PASSWORD=your_db_password
DB_HOST=db
DB_PORT=5432
```

## Update Domain Name
Edit *nginx/hallow.conf*, change the *server_name* directive with your domain name.  
Edit *vue_hallow/src/storage/service.js*, change the *API_HOST* const with your domain name.

## Build Containers
```
docker-compose up -d --build

docker exec -it hallowdjangovue_django /bin/sh
/app # python manage.py migrate
/app # python manage.py createsuperuser --username=your_username --email=your_email
```