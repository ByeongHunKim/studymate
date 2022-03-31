# studyMate

## Hyperledger Fabric 1.4 LTS 

## pre-condition

- `curl 7.68.0` , `docker 20.10.7` , `docker-compose 1.25.0` , `go 1.15.15` , `hyperledger fabric-docker images` , `hyperledger bineries cryptogen, configtxgen..` , `configured GOPATH`  

---

## stack

### Blockchain
![Hyperledger](https://img.shields.io/badge/hyperledger-2F3134?style=for-the-badge&logo=hyperledger&logoColor=white)

### Operating Sysyem
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)

### Languages
![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Shell Script](https://img.shields.io/badge/shell_script-%23121011.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
<img src="https://img.shields.io/badge/html-E34F26?style=for-the-badge&logo=html5&logoColor=white">
<img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white">

### Frameworks, Platforms and Libraries
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=%2361DAFB)
![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![jQuery](https://img.shields.io/badge/jquery-%230769AD.svg?style=for-the-badge&logo=jquery&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-%23000000.svg?style=for-the-badge&logo=npm&logoColor=white)
![Bootstrap](https://img.shields.io/badge/bootstrap-%23563D7C.svg?style=for-the-badge&logo=bootstrap&logoColor=white)

### Other 
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)


## Test Report

### First you need to check you stutus 1. docker container, 2. docker images and docker network
### for check your status,
1. `docker ps -a`
2. `docker images`
3. `docker network ls`

---

### this is the clean status

![cleanStatus](./images/cleanStatus.PNG)

---
### if u have some container, images or network please remove all
1. `docker rm -f $(docker ps -aq)` 
2. `docker rmi -f $(docker images dev-* -q)` 
3. `docker network prune` and y

---
### A. network 

- cd network 
    - `./generate.sh`

    -  `./start.sh`

---

### B. contract
- cd contract
    - `ls` -> `cc_study_v1.0.sh , studymate.go`
    
    - `./cc_study_v1.0.sh instantiate v1.0`

- check chaincode whether installed, instantiated or not
    - `docker exec cli peer chaincode list --installed`
    - `docker exec cli peer chaincode list --instantiated -C mychannel`

---

### C. prototype
- cd prototype
    - `npm install`

- certification works
    - `node enrollAdmin.js`
    - `node registerUser.js`
---
### Server start

- `node server.js`

---

### D. open ip OR localhost:8080 in the website

![networkCommand](./images/networkCommand.PNG)
![prototypeResult](./images/prototypeResult.PNG)

---

### E. ip OR localhost:5984 is couchDB
---
![db](./images/db.PNG)
---

### F. hyperledger-explorer
---
![explorerSuccess](./images/explorerSuccess.PNG)
---
## Issue List
- port fowarding -> 22[ssh], 3000[prototype], 8080[hyperledger-explorer], 5984[couchdb] 
- 
---

## Update plan

- add nodemon
- connect with Hyperledger Explorer -------- success 0401 07:29 AM
- refactoring using react


---
