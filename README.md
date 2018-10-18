# ELK_DOCKER

33START FROM SCRATCH

#sudo docker pull sebp/elk 


#sudo docker run -p 5601:5601 -p 9200:9200 -p 5044:5044 -it --name elk sebp/elk

## ADD VOLUM ON START DOCKER
k/run


##Install PING COMMAND and COMMIT on V2 Images

#apt-get install iputils-ping

#sudo docker commit -m "install iputils-ping " elk-nagios sebp/elk:v2



## redierct some log to enable kabana

#sudo docker exec -it elk /bin/bash
#/opt/logstash/bin/logstash --path.data /tmp/logstash/data -e 'input { stdin { } } output { elasticsearch { hosts => ["localhost"] } }'







