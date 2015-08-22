# logstash

[![Join the chat at https://gitter.im/mesoscloud/logstash](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/mesoscloud/logstash?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Logstash

https://www.elastic.co/products/logstash

## CentOS

[![](https://badge.imagelayers.io/mesoscloud/logstash:1.5.4-centos-7.svg)](https://imagelayers.io/?images=mesoscloud/logstash:1.5.4-centos-7)

e.g.

```
docker run -d \
-v /srv/events:/srv/events \
-v /srv/logstash:/srv/logstash \
--name=logstash --restart=always mesoscloud/logstash:1.5.4-centos-7 logstash -e 'input { file { path => "/srv/events/containers.log-*" codec => json sincedb_path => "/srv/logstash/sincedb" } } output { elasticsearch { } }'
```

## Ubuntu

[![](https://badge.imagelayers.io/mesoscloud/logstash:1.5.4-ubuntu-14.04.svg)](https://imagelayers.io/?images=mesoscloud/logstash:1.5.4-ubuntu-14.04)

e.g.

```
docker run -d \
-v /srv/events:/srv/events \
-v /srv/logstash:/srv/logstash \
--name=logstash --restart=always mesoscloud/logstash:1.5.4-ubuntu-14.04 logstash -e 'input { file { path => "/srv/events/containers.log-*" codec => json sincedb_path => "/srv/logstash/sincedb" } } output { elasticsearch { } }'
```
