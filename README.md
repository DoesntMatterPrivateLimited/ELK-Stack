# ELK Stack Configure

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

Add “discovery.type: single-node”
















































































