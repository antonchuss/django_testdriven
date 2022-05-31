# DEV
docker-compose up -d --build

# PROD
docker-compose -f docker-compose.prod.yml up -d --build <br>
docker-compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput <br>
docker-compose -f docker-compose.prod.yml exec web python manage.py collectstatic --no-input --clear <br>

