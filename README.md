# ELK Stack Configure

Prerequisites:
  
  - Java 8 or 11 supported

```
sudo apt update -y
sudo apt install openjdk-11-jre-headless -y
java -version
```  

Add the elasticsearch APT repository key by using the below command:

```
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
```
