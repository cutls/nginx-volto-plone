cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html

[Japanese](README.ja.md)

1. default.sample.conf を default.conf にリネーム
1. default.certbot.sample.conf を default.certbot.conf にリネーム
1. default.conf や default.certbot.conf 内にある`mydomain.tld`を動かしたいドメインに置換する
1. run `sudo docker compose -f docker-compose-initial.yml up -d`
1. run `sudo docker-compose run --rm certbot certonly --webroot -w /var/www/html -d mydomain.tld`(mydomain.tldは自分のドメインに置換)
1. run `sudo docker compose up -d`(-dを付けることでデーモン化され、compose downするまで動き続けます。)
