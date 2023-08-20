cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html

1. `git clone https://github.com/cutls/nginx-volto-plone`
1. `cd nginx-volto-plone`
1. default.sample.conf を default.conf にリネーム
1. run `sudo docker compose up` (`sudo docker compose up -d`でデーモン化され、compose downするまで起動し続けます)

"letsencrypt"ブランチは、httpsで実運用する用に書かれています。