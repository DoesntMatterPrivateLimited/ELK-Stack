# ELK Stack Configure on ubuntu 22.04

Prerequisites:
  
  - Java 8 or 11 supported

```
sudo apt update -y
sudo -i
sudo apt install openjdk-11-jre-headless -y
java -version
```  

Add the elasticsearch APT repository key by using the below command:

```
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
```

Add the elastic to the APT source list by using the below command:

```
echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
```

Update the APT source list by using the below command:

```
apt update
```

Install the Elastic Search by using the below command:

```
apt install elasticsearch -y
```

Configure the elasticsearch by using the below command:

```
vim /etc/elasticsearch/elasticsearch.yml
```
Change the network.host and http.port as per the screenshot(network.host is the IP of the Ubuntu machine)

Just below, find the Discovery section. We are adding one more line, as we are configuring a single node cluster:
Add “discovery.type: single-node”

![Screenshot ](https://i.imgur.com/IUNFAJ0.png)

Configure the JVM heap memory by using the below command:

```
vim /etc/elasticsearch/jvm.options
```
  -Xms512m , 
  -Xmx512m

![Screenshot ](https://i.imgur.com/MNGFjaY.png)













































































