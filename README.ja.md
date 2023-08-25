cf: https://6.docs.plone.org/install/containers/examples/nginx-volto-plone.html
cf: https://6.docs.plone.org/volto/deploying/apache.html

`apachectl -v`でApacheのバージョンが2.4以上であることを確認してください。

1. `git clone https://github.com/cutls/nginx-volto-plone`
1. `cd nginx-volto-plone`
1. docker-compose.sample.yml を docker-compose.yml にリネーム
1. docker-compose.ymlの`RAZZLE_API_PATH`を自分のドメインに編集
1. apache.confの 21, 22, 23, 17, 28, 32, 33, 34, 27, 40行目にある`domain.tld`を自分のドメインに編集
1. `apache.conf`をApacheの構成ファイルの所定場所に置きます。(ex: `/etc/apache2/sites-available`)
1. **必要なApacheモジュールを有効にします**: `lbmethod_bybusyness` `proxy_http` `ssl` `headers`
   * `sudo a2enmod lbmethod_bybusyness proxy_http ssl headers`
1. Apache2サーバを再起動します。
1. default.sample.conf を default.conf にリネーム
1. run `sudo docker compose up` (`sudo docker compose up -d`でデーモン化され、compose downするまで起動し続けます)
