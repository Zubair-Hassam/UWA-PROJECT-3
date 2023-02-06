# MERN Stack Application

## Project Description
As the bootcamp has reached its climax, a test was put forward to test our knowledge and capabilities by having us create a MERN Stack single-page application. The overall idea is to have a landing page which offers some form of functionality, whilst also maintaining a database of users that are able to possibly make payments. 

## Conceptual Idea
The direction which i took this challenge was retail. The application built is an online store which offers different products from around the world for people to purchase. Individuals also have their own profiles allowing them to have personiled experiences. 

## User Story 
As a shopper interested in buying items 
I want to be able to browse products on the site 
So that I can buy the most suitable product 

## Technologies utilised 
```
React 
GraphQL
MongoDB
Mongoose
Heroku
JWT
Stripe
```


## Deployement Instructions 
1. #### clone the repo using this command
    ```bash
    git clone https://github.com/Zubair-Hassam/UWA-PROJECT-3.git
    ```
2. #### install npm packages
    1. install backend packages
    ```bash
    cd Shopify
    npm install
    ```
    2. install frontend packages
    ```bash
    cd client
    npm install
    ```
3. go to the parent folder of Shopify & create .env for mongodb connection, JWT_SECRET, BRAINTREE_MERCHANT_ID, BRAINTREE_PUBLIC_KEY and BRAINTREE_PRIVATE_KEY.

    ##### sample code for backend .env
    ```env
    MONGO_URI=YOUR_MONGO_URI
    JWT_SECRET=YOUR_JWT_SECRET
    BRAINTREE_MERCHANT_ID=YOUR_BRAINTREE_MERCHANT_ID
    BRAINTREE_PUBLIC_KEY=YOUR_BRAINTREE_PUBLIC_KEY
    BRAINTREE_PRIVATE_KEY=YOUR_BRAINTREE_PRIVATE_KEY
    ```
4.  create another .env file inside client directory for REACT_APP_API_URL.
    
    ##### sample code for frontend .env
    ```env
    REACT_APP_API_URL=YOUR_API_URL
    ```
    ##### Instruction:
    1. for mongodb atlas database creation follow this tutorial->https://www.youtube.com/watch?v=KKyag6t98g8
    2. you can use any random string as JWTSECRET
    3. for localhost REACT_APP_API_URL is http://localhost:5000/api
       but for heroku (server deployment) it will be different
    4. #### note: add .env on .gitignore
    5. for server deployment use secrets directly

5. <b>deploy this project</b> on your local server by using this command
    ```bash
    cd Shopify
    npm run server
    ```
    <b>In another terminal/power shell</b>
    ```bash
    cd Shopify\client
    npm start
    ```
    #### note: both backend & frontend server will start with the above commands.

6. #### Database Structure: (Table: columns)
    1. categories: _id, name, createdAt, updatedAt;
    2. orders:  _id, status, products (Array), transaction_id, amount, address, user (Object), createdAt, updatedAt
    3. products: _id, photo (Object), sold, name, description, price, category, shipping, quantity, createdAt, updatedAt
    4. users: _id, role, history (Array), name, email, salt, hashed_password, createdAt, updatedAt

## Authors
    Zubair Hassam

