# Instruction to set up a performance test environment
## Set up a centos 8 server
```shell
$ sudo yum -y update
$ sudo yum install -y git
$ sudo systemctl enable firewalld
$ sudo systemctl start firewalld
$ sudo firewall-cmd --permanent --zone=public --add-port=8080/tcp
```

## clone the jpetstore application
```shell
$ git clone https://github.com/mybatis/jpetstore-6.git
```
## Build war file
```shell
$ cd jpetstore-6
$ ./mvnw clean package
```
