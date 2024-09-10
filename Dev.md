

## DB
Create DB

ssh appfx
ship exec db bash
mysqldump -uroot -p koel > /temp/koel_2024_09_09

mv /srv/bay/dbsttore/data/temp/koel_2024_09_09 ~

scp appfx:~/koel_2024_09_09 .
mysql -uroot -p koel < koel_2024_09_09

## Init
composer install
npm install --global yarn
php artisan koel:init --no-interaction


## Dev
yarn dev
localhost:8000
