### 步骤记录
* 用户注册和application 创建
* 下载和安装heroku工具
* heroku login
* 添加key https://devcenter.heroku.com/articles/keys
* cd qiankun
* git push git@heroku.com:qiankun.git master
* config heroku production database  heroku config --app qiankun | grep HEROKU_POSTGRESQL
* change production database username and password to heroku username and password
*  HEROKU_POSTGRESQL_AMBER_URL: postgres://zwsbwlwwxbpjnp:PY8IuSxw5xhTpKHPdTXLxeETF
O@ec2-54-197-241-96.compute-1.amazonaws.com:5432/dcqct4b17c963r

* heroku run rake ar:create --app qiankun
* heroku run rake ar:migrate --app qiankun
* heroku run rake db:migrate

