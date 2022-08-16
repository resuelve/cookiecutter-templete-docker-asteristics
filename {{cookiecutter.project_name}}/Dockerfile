FROM {{ cookiecutter.org_name }}/{{ cookiecutter.project_name }}:{{ cookiecutter.deploy_image_version }}

COPY .env /var/www
RUN cd /var/www && php artisan key:generate
# RUN php artisan migrate
# RUN php artisan config:clear
RUN php artisan optimize
# RUN php artisan config:cache
