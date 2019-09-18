# docker-compose-parse-server
* Parse Server docker  -  all in one docker-compose.yml file.
  * nginx
  * mongodb
  * postgres
  * parse-server
  * parse-dashboard
  * parse_live
  * portainer
* flutter client parse_live url setting:const String keyParseLiveServerUrl = 'http://yourhostip:1337/api/';
* run docker
```shell
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
$ sudo chmod +x /usr/local/bin/docker-compose
$ docker-compose --version
$ sudo docker-compose up -d 
$ docker-compose ps
$ docker-compose down
$ docker-compose down --volumes
$ docker-compose restart
$ docker volume create portainer_data 
```
* test data
```shell
curl -X POST \
-H "X-Parse-Application-Id: APPLICATION_ID" \
-H "Content-Type: application/json" \
-d '{"score":1337,"playerName":"Sean Plott","cheatMode":false}' \
http://host ip/bas/classes/GameScore
```
