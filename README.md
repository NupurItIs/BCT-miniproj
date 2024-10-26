# BCT-miniproj
miniproj for bct lab 



# DigiPolls

DigiPolls focuses on creating a blockchain-based e-voting solution using the Ethereum platform and Solidity language. It aims to provide a secure, transparent, and private voting system. By leveraging blockchain technology, the project ensures that each vote is securely recorded and verifiable, protecting voter anonymity while preventing fraud and manipulation.


For more details checkout our [Project report](https://github.com/NupurItIs/BCT-miniproj/blob/main/report.pdf)
## Motivation



Will of people forms the basis of democracy.However it is of utmost importance to protect the anonymity of voters and allow complete privacy to cast their votes.The current methodology may sometimes fail to protect the fundamental right of privacy of the voters. The master key to build an electronic voting system is to find out a secure underlying platform which provides the required features that overcomes the drawbacks of the current system. 



## Features

- Intuitive Voting Interface
- Blockchain Security
- Core Functionalities
- Centralized Management
- Browser Accessibility
- Scalable Architecture
- Secure Authentication (JWT)
- Ethereum Integration
- Admin Panel



## Technologies

- Node.js  
- Web3.js 
- Truffle 
- Solidity 
- Ganache 
- Metamask
- Python
- FastAPI
- MySQL Database


## Functionality 

User enters the credentials (voter id & password) and they are matched with the database. If the match is found user is either redirected to admin page or voter page as per their role corresponding to the credentials in the database. Once the admin is logged in he/she can start the voting process by adding candidates and defining dates. Voter can vote once the voting process has been started. Once the voter has voted the transaction is recorded to the blockchain and the voting page is updated with real-time votes.




## Installation

1. Open a terminal.

2. Clone this repository. 
```
   git clone https://github.com/NupurItIs/BCT-miniproj.git
```
    
3. Download and install [Ganache](https://archive.trufflesuite.com/ganache/) .

Create a workspace named developement, in the truffle projects section add `truffle-config.js` by clicking `ADD PROJECT` button.

5. Download [Metamask](https://metamask.io/download/) extension for the browser. 


Now create wallet (if you don't have one), then import accounts from ganache.

7. Add network to the metamask. ( Network name - Localhost 7575, RPC URl - http://localhost:7545, Chain ID - 1337, Currency symbol - ETH)

8. Open MySQL and create database named voter_db in mysql

In the database created, create new table named voters in the given format and add some values.

    CREATE TABLE voters (
    voter_id VARCHAR(36) PRIMARY KEY NOT NULL,
    role ENUM('admin', 'user') NOT NULL,
    password VARCHAR(255) NOT NULL
    );


Install truffle globally
```
npm install -g truffle
```

Go to the root directory of repo and install 
node modules

```
npm install
```

Install python dependencies

```
pip install fastapi mysql-connector-python pydantic python-dotenv uvicorn uvicorn[standard] PyJWT

```






## Run locally


1. Update the database credentials in the `./Database_API/.env` file.


2. open terminal in project's root directory and run the command

 ```
 truffle console
```
then compile the smart contracts with command
```
 compile
 ```
exit the truffle console


3. Bundle app.js with browserify

 ```
 browserify ./src/js/app.js -o ./src/dist/app.bundle.js
 ```

4. Start server

 ```
 node index.js
 ```

5. Navigate to Database_API folder in another terminal
```
 cd Database_API
 ```

then start the database server by following command
```

 uvicorn main:app --reload --host 127.0.0.1
 ```

6. In a new terminal 
```
 truffle migrate
 ```


The app should be up and running now at http://localhost:8080/.



## Screenshots

![App Screenshot](https://github.com/NupurItIs/BCT-miniproj/blob/main/public/g1.png)
![App Screenshot](https://github.com/NupurItIs/BCT-miniproj/blob/main/public/i1.png)
![App Screenshot](https://github.com/NupurItIs/BCT-miniproj/blob/main/public/t1.png)
![App Screenshot](https://github.com/NupurItIs/BCT-miniproj/blob/main/public/m1.png)


## Contributing

Contributions are always welcome!


Please adhere to this project's `code of conduct`.


## Authors

- [@virajbhansali7](https://github.com/virajbhansali7)

- [@Tashbhilare](https://github.com/Tashbhilare)

- [@NupurItIs](https://github.com/NupurItIs)


