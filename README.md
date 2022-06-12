# NonTextNeck


## InfluxDB 설치방법

  0.라즈베리파이 업데이트
  ```
  sudo apt update
  sudo apt upgrade
  ```
  1.Respository의 GPG key더하기
  ```
  wget -qO- https://repos.influxdata.com/influxdb.key | sudo apt-key add -
  ```
  2.Respository를 더하기
  ```
  echo "deb https://repos.influxdata.com/debian stretch stable" | sudo tee /etc/apt/sources.list.d/influxdb.list
  ```
  3.프로그램 설치
  ```
  sudo apt update
sudo apt install influxdb
```
  3.프로그램 실행 설정
  ```
  sudo systemctl unmask influxdb
sudo systemctl enable influxdb
sudo systemctl start influxdb
```
  4.데이터베이스 만들기
  ```
  $ influx

>create database <데이터베이스이름>
  확인법 : show databases
```  
  Grafana 설치방법
  
  1. Repository의 GPG key 더하기
  ```
  wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
  ```
  2.Respository 더하기
  ```
  echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
  ```
  3. 프로그램 설치
  ```
  sudo apt update
sudo apt install grafana
```
  4.프로그램 실행
  ```
  sudo service grafana-server start
  ```
  influxdb에서 python의 데이터 가져오는 코드
  ```
  sudo pip3 install influxdb
  ```
  gpio 핀맵
  ```
  cd /tmp
wget https://project-downloads.drogon.net/wiringpi-latest.deb
sudo dpkg -i wiringpi-latest.deb
```
