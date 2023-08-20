cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html

[Japanese](README.ja.md)

1. `git clone https://github.com/cutls/nginx-volto-plone`
1. `cd nginx-volto-plone`
1. RENAME default.sample.conf to default.conf
1. run `sudo docker compose up` (`sudo docker compose up -d` to be a daemon)

Check "letsencrypt" branch to run as production with https