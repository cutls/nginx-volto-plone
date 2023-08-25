cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html
cf: https://6.docs.plone.org/volto/deploying/apache.html

[Japanese](README.ja.md)

run `apachectl -v` to check your Apache2 is above 2.4!

1. `git clone https://github.com/cutls/nginx-volto-plone`
1. `cd nginx-volto-plone`
1. RENAME docker-compose.sample.yml to docker-compose.yml
1. add `RAZZLE_API_PATH` to your domain in docker-compose.yml
1. replace `domain.tld` to your domain in line 21, 22, 23, 17, 28, 32, 33, 34, 27, 40 of apache.conf to your domain
   * line 32-34 is config about https. Check you have available certs on the folder(example uses Let's Encrypt)
1. move `apache.conf` to your apache config directory(ex: `/etc/apache2/sites-available`)
1. **This apache config file requires some modules**: `lbmethod_bybusyness` `proxy_http` `ssl` `headers`
   * `sudo a2enmod lbmethod_bybusyness proxy_http ssl headers`
1. restart your apache2 server
1. RENAME default.sample.conf to default.conf
1. run `sudo docker compose up` (`sudo docker compose up -d` to be a daemon)

Check "letsencrypt" branch to run as production with https