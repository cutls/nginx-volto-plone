cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html

1. RENAME default.sample.conf to default.conf
1. RENAME default.certbot.sample.conf to default.certbot.conf
1. replace `mydomain.tld` to your domain in default.conf and default.certbot.conf
1. run 
1. run `sudo docker-compose run --rm certbot certonly --webroot -w /var/www/html -d mydomain.tld`
