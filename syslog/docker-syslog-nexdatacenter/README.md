# DOCKER-SYSLOG Firstwap | IMPORTANT !!!#

FHS Docker Syslog-ng :
```
   log
    |
    |----------config
    |             |-----conf.d
                  |-----Docker-Builds
                             |--syslog
                             |--tftp
                  |-----docker-compose.yml
    |----------network
    |----------os
```


## Information ##
Directory **Config** is important, we can build any service in this directory.


### How To Build and Running Service ###
How to build and running docker with docker-compose? except docker compose we can run manual using **_docker run_**.
The following command build and run using docker-compose :


### Syslog-networks ####
** Build **
> `cd /log/config`
> `docker-compose build syslog-networks`


** Running **
> `cd /log/config`
> `docker-compose start syslog-networks`


** Build and Running **
>`cd /log/config`
>` docker-compose up -d --build syslog-networks`


### How Check Service Running ###
Standard to check service using :
> `docker ps`


check all service using :
> `docker ps -a`


### How Start, Stop And Restart Service  ###
stop service in container
> `docker stop syslog-networks`


start service in container
> `docker start syslog-networks`


restart service in container
> `docker restart syslog-networks`

