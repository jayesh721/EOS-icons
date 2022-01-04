# EOS Icons
Enhancing the backend behind EOS-icons and introducing new features
![alt text](https://github.com/iifawzi/GSOC-2021-Project-Report/raw/master/assets/eos-icons.jpeg)

## EOS Icon Picker
[![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)

## Main Changes
- The code got re-written in `typescript`.
- `MongoDb` is used as the database. 
- A `Docker` image is created to encapsulate everything for easier running and deployment process.
- Unit tests are written using `chai` and `mocha` to ensure that all the new APIs are working as expected.
- A validation layer using `Joi` is added to validate all the incoming requests.
- Caching layer is introduced to make the process of fetching the icons faster.
- Algolia services is introduced to be used for the search queries.

<br/>

### Technologies used:
`Typescript`, `javascript`, `Node.js`, `Docker`, `MongoDB`, `Redis`, `Algolia`, `Mocha`

<br/>

### Overview of the project:
![diagram](https://user-images.githubusercontent.com/68469442/148102640-3ed03713-ca79-4e84-a66a-b2c84e2a739b.PNG)

## Running the project

- Cloning the repo:
````
git clone https://github.com/EOS-uiux-Solutions/eos-icons-api
````
- Once the repository is cloned, You can choose the way you prfer: 

### | Using Docker: 
  By using our docker image, we will take care of everything</br> 
  - **Steps**:
    - Install docker using'https://docs.docker.com/engine/install/ubuntu/'
    - Modify the `REDISCLOUD_URL` enviroment variable to `redis://redis:6379` in the environment variable folder.
    - Modify the `MongoURI` enviroment variable to `mongodb://mongo:27017/eosiconsdb` in the environment variable folder.
    - From within the cloned respository run the following command to build the image: </br>
  ````
  docker-compose up
  ````
  - Your server container will be started at `http://localhost:3131`
  - Mongo database can be accessed from MongoDB compass at `mongodb://mongo:27017/eosiconsdb`

### | Running on your machine:
  - **Steps**:
    - Install the required python dependencies:
      - On Linux: 
        ```
        sudo apt-get install fontforge ttfautohint
        ```
    - Install Visual Studio
      https://linuxize.com/post/how-to-install-visual-studio-code-on-ubuntu-20-04/
    - Install MongoDB: 
      https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/
    - Install Redis: 
      https://www.digitalocean.com/community/tutorials/how-to-install-and-secure-redis-on-ubuntu-20-04
    - Install Postman tests:
      https://learning.postman.com/docs/getting-started/installation-and-updates/#installing-postman-on-linux
    - Install Mocha
      https://riptutorial.com/mocha/example/27433/installation-or-setup
    - Install Chai
      https://www.npmjs.com/package/chai
    - Install joi : npm install joi
    - Install Swagger:
      https://www.npmjs.com/package/swagger
    - Install MongoDB Compass:
      https://docs.mongodb.com/compass/current/install/
     
    - Install the dependenices and run the server: 
    1. Install dependencies using `npm install`
    2. Install grunt globally `npm install -g grunt-cli`
    3. Start the server using `npm start`
    - Your server will be started at `http://localhost:3131`
    - 
- Run the tests after any modification, or add new one for any addition. 
1. For `V1` APIs we're using Postman tests, which can be started using `npm run test:v1`
2. For `V2` APIs we're using Mocha tests, which can be started using `npm run test:v2`
3. Test All the APIs using `npm run test` 
