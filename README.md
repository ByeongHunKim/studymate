# studyMate

## Hyperledger Fabric 1.4 LTS 

---
A. network 

- cd network 
    - ./generate.sh

    -  ./start.sh

B. contract
- cd contract
    - ls -> cc_study_v1.0.sh , studymate.go
    
    - ./cc_study_v1.0.sh instantiate v1.0

- check chaincode whether installed, instantiated or not
    - docker exec cli peer chaincode list --installed
    - docker exec cli peer chaincode list --instantiated -C mychannel

C. prototype
- cd prototype
    - npm install

- certification works
    - node enrollAdmin.js
    - node registerUser.js
- server start
    - node server.js

