# Instruction to set up a performance test environment
## Set up a centos 8 server
```shell
$ sudo yum -y update
$ sudo yum install -y git maven java
$ sudo systemctl enable firewalld
$ sudo systemctl start firewalld
$ sudo firewall-cmd --permanent --zone=public --add-port=8080/tcp
$ sudo firewall-cmd --reload
```

## clone the jpetstore application
```shell
$ mkdir ${HOME_DIR}/Documents/application
$ cd ${HOME_DIR}/Documents/application/
$ git clone https://github.com/kazuki43zoo/mybatis-spring-boot-jpetstore.git
```
## Build jar file
```shell
$ cd mybatis-spring-boot-jpetstore.git
$ ./mvnw clean package -DskipTests=true
$ java -jar target/mybatis-spring-boot-jpetstore-2.0.0-SNAPSHOT.jar
```
