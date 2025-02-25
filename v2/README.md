# Update Selected User using Admin Profile

You can use below link to know how to create this app

https://available-soon

**If you face any error after doing below steps, then please update current version of your installed NodeJS software.**

## Starting Code (Base code)

Repositry Number: T21

## Versions Detail

### Version 0 (v0)

- no glables.css

## How to Run:

- Open folder for any version
- Open this folder with VS Code
- Open VS code terminal and type command

      npm install

- Above command will install all neccessary packages and create node_modules folder in your downloaded code.

- Now run below command to run this app

      npm run dev

- env.local file is necessary. Rename env.txt file as .env.local

- Import database into MongoDB Compass:

      1. Open MongoDB Compass.
      2. Create new database named as "team_manager_db" and collection name as "register_user". These names are defined in src/app/api/register/route.ts
      3. Database name is also used in .env.local file
      4. If you want to add our created-data, then you can follow below instructions.
            a. Before proceed instructions, it is noted that if you already created data, then unique ID may be duplicated with our Data-IDs. Therefore, be carefull otherwise database-error may rise.
            Create database and collection as mentioned above.
            b. Navigate to the database and click on "Add Data" > "Import File"
            c. Select the team_manager_db.register_user.json file and import it into the appropriate collection

# Update in v2

This repo is made keeping in mind the v1, only change in this repo is that:

## Problem in v1

In v1 if User and Admin have same credentials and Login through eather Portel ie userLogin or AdminLogin if the token of one is availabe in the browser they can login.

## Solution in v2

So to distinguish between user and admin i have defined the "GetUserType" function in "utils/token.ts". This function will help us distinguish between the user and admin token.
note that this function is defined the Function in the "utils/token.ts" file and used it in the "src/app/api/auth/token/route.ts".
