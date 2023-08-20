cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html

[Japanese](README.ja.md)

1. RENAME default.sample.conf to default.conf
1. RENAME default.certbot.sample.conf to default.certbot.conf
1. replace `mydomain.tld` to your domain in default.conf and default.certbot.conf
1. run `sudo docker compose -f docker-compose-initial.yml up -d`
1. run `sudo docker-compose run --rm certbot certonly --webroot -w /var/www/html -d mydomain.tld`
1. run `sudo docker compose up -d`
