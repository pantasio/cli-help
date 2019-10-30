### Create a bridge network with a subnet and gateway:
'''
docker network create --subnet 10.1.0.0/24 --gateway 10.1.0.1 br02
'''

### Create a network with an IP range:
'''
docker network create --subnet 10.1.0.0/16 --gateway 10.1.0.1 --ip-range=10.1.4.0/24 --driver=bridge --label=host4network br04
'''

## Networking two containers

### Create an internal network:
'''
docker network create -d bridge --internal localhost
'''

### Create a MySQL container that is connected to localhost
'''
docker container run -d --name test_mysql -e MYSQL_ROOT_PASSWORD=P4sSw0rd0 --network localhost mysql:5.7
'''

### Create a container that can ping the MySQL container
'''
docker container run -it --name ping-mysql --network bridge centos
'''

### Connect ping-mysql to the localhost network
'''
docker network connect localhost ping-mysql
'''
