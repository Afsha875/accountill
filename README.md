### [accountill.com](https://accountill.com/)
# MERN Stack Invoicing Application
Built with the MERN stack (MongoDB, Express, React and NodeJS).
![Invoice](https://res.cloudinary.com/almpo/image/upload/v1637311386/invoice/invoice-app_tcz0dj.png)


## Update
I am pleased to inform you that the name of this repository has been changed from Arc Invoice to Accountill.
There are many new features and improvements in the pipeline. Stay tuned.


Afsha
----

  * [Introduction](#introduction)
  * [Key Features](#key-features)
  * [Technologies used](#technologies-used)
      - [Client](#client)
      - [Server](#server)
      - [Database](#database)
  * [Configuration and Setup](#configuration-and-setup)
  * [Troubleshooting](#troubleshooting)
  * [Author](#author)
  * [License](#license)

## Introduction
This is a comprehensive invoicing application built using the MERN stack (MongoDB, Express, React and Nodejs). It is specifically designed for freelancers and small businesses, but it is versatile enough for almost any business need. With this application, you can generate and send professional invoices, receipts, estimates, quotes, and bills to your clients. You can explore the [Live App](https://accountill.com/) to start sending invoices immediately or review the source code to run it on your own server. This project is maintained in my professional interest to provide a reliable tool for business management. I appreciate any feedback or issue reports to help improve the platform.

![Invoice Dashboard](https://res.cloudinary.com/almpo/image/upload/v1637314504/invoice/dashboard_c5z0is.png)

## Key Features
- Send invoices, receipts, estimates, quotations and bills via email
- Generate and send/download pdf invoices, receipts, estimates, quotations and bills via email
- Set due date
- Automatic status change when payment record is added
- Payment history section for each invoice with record about payment date, payment method and extra note
- Record partial payment of invoice
- Clean admin dashboard for displaying all invoice statistics including total amount received, total pending, recent payments, total invoice paid, total unpaid and partially paid invoices
- Multiple user registration
- Authentication using jsonwebtoken (jwt) and Google auth


## Technologies used
This project was created using the following technologies.

#### Client

- React JS
- Redux (for managing and centralizing application state)
- React-router-dom (To handle routing)
- Axios (for making api calls)
- Material UI and CSS Module (for User Interface)
- React simple Snackbar (To display success/error notifications)
- Cloudinary (to allows users to upload their business logo)
- Apex Charts (to display payment history)
- React-google-login (To enable authentication using Google)

#### Server

- Express
- Mongoose
- JWT (For authentication)
- bcryptjs (for data encryption)
- Nodemailer (for sending invoice via email)
- html-pdf (for generating invoice PDFs)

#### Database
MongoDB (MongoDB Atlas)

## Configuration and Setup
In order to run this project locally, clone the repository or download the source files to your machine. 
- Open the project in your preferred code editor.
- Go to terminal -> New terminal.
- Split your terminal into two (run the client on one terminal and the server on the other terminal).

In the first terminal
- cd client and create a .env file in the root of your client directory.
- Supply the following credentials:

```
REACT_APP_GOOGLE_CLIENT_ID = 
REACT_APP_API = http://localhost:5000
REACT_APP_URL = http://localhost:3000

```

To get your Google ClientID for authentication, go to the credential Page (if you are new, then create a new project first) and follow these steps:

- Click Create credentials > OAuth client ID.
- Select the Web application type.
- Name your OAuth client and click Create.
- Remember to provide your domain and redirect URL so that Google identifies the origin domain to which it can display the consent screen. In development, that is going to be http://localhost:3000 and http://localhost:3000/login.
- Copy the Client ID and assign it to the variable REACT_APP_GOOGLE_CLIENT_ID in your .env file.

```
$ cd client
$ npm install
$ npm start
```
In the second terminal
- cd server and create a .env file in the root of your server directory.
- Supply the following credentials:

```
DB_URL = 
PORT = 5000
SECRET = 
SMTP_HOST = 
SMTP_PORT = 
SMTP_USER = 
SMTP_PASS = 

```

Please follow standard documentation to create your mongoDB connection url, which you will use as your DB_URL.

```
$ cd server
$ npm install
$ npm start
```

## Troubleshooting
If you encounter errors while trying to send or download PDF files, please run the following commands in your server terminal:

```
$ npm install html-pdf -g
$ npm link html-pdf
$ npm link phantomjs-prebuilt
```

## Docker

Using docker is straightforward. Add the .env file contextualized with the docker network.

Example for "server/.env":
```
DB_URL = mongodb://mongo:27017/arch
PORT = 5000
SECRET = 
SMTP_HOST = 
SMTP_PORT = 
SMTP_USER = 
SMTP_PASS = 
```
Example for "client/.env":
```
REACT_APP_GOOGLE_CLIENT_ID = 
REACT_APP_API = http://localhost:5000
REACT_APP_URL = http://localhost
```

And run:

```
docker-compose -f docker-compose.prod.yml build

docker-compose -f docker-compose.prod.yml up
```

## Comment
I intend to keep adding more features to this application. If you find this project useful, please consider giving it a star to support continued development and improvements.


## Author

- Maintainer: Afsha Fathima
- Email: fathimaafsha08@gmail.com
- LinkedIn: https://www.linkedin.com/in/afsha-fathima-lnu-a29996298/
- Original Creator: Panshak

## About the Developer
Afsha Fathima is a Backend Developer with over 4 years of experience building scalable applications, REST APIs, and business-critical software. With a strong foundation in Python, SQL, and various database technologies, she focuses on developing maintainable backend solutions and improving application performance. Her expertise spans across financial services and enterprise technology environments, with additional experience in C# and AI integrations.

## License

- This project is MIT licensed.