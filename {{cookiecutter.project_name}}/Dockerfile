FROM {{ cookiecutter.org_name }}/{{ cookiecutter.project_name }}:{{ cookiecutter.deploy_image_version }}

COPY .env /var/www
RUN php artisan key:generate

RUN php artisan optimize
