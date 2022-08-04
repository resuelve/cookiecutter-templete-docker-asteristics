FROM resuelve/asteristics:master-07f094d

COPY .env /var/www
RUN php artisan key:generate

# RUN php artisan migrate
# RUN php artisan config:clear
RUN php artisan optimize
# RUN php artisan config:cache
