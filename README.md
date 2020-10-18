Welcome to cf-redis-commander-SSL
===================

Overview
-------------

Wrapper of redis-commander for cloud foundry.
Thanks to https://github.com/joeferner/redis-commander/.
The code in this repository supports redis cache instance which is enabled TLS/SSL (like Amazon ElasticCache)

----------
Deployment to Cloud Foundry
-------------
1) git clone this repository,
```
git clone https://github.com/bitcat1973/cf-redis-commander
cd cf-redis-commander
```
Remember to install [cf cli](https://github.com/cloudfoundry/cli/releases) and then get an account from [Pivotal Web Services](http://run.pivotal.io/).

2) Modify the binding service name in manifest file
    replace string 'ss-redis-new' with your service name in manifest file

3) SSL is enable by default. To turn off SSL, you can change value of SSL to false in manifest file

3) Push the application:
```
cf push 
```

5) You can access your app at 
```
http(s)://cf-redis-commander-ssl.{{your domain}}
credential is admin/pass
```