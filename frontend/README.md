# Prodcut Management System
This is a React-based Product Management App that allows users to add, view, edit, and delete products with a name, price, and image. It uses Chakra UI for styling, Axios for API calls, and connects to a backend built with Node.js, Express, and MongoDB. Products are managed in real-time using React state and displayed in a responsive grid. Users can upload images (converted to base64), and edit product details inline. The app includes smooth background animation, SEO optimization via react-helmet, and follows clean component structure and good React practices.

## Prerequisites How to run
- NodeJS version 22.X

###  How to run Web Server
The webserver is ExpressJs running on NodeJS runtime engine. on the root folder of the repository run the following commands
- `npm install`
- `npm run dev`
  
If it runs successfully, you'll see the message: MongoDB connected: via MongoDB Atlas

###  How to run Frontend
From the root folder of the repository change into `frontend` folder and run the following commands in the provided sequence
- `npm install`
- `npm run dev`
    
## Technology Stack

### Frontend
- ReactJs
- Chakra UI
- Axios API Library

### Backend
- ExpressJS web server with NodeJs
- Mongoose Database Access Library
- MongoDB

  ## 1: HTTP Verbs (4 used)

 GET → getProducts

POST → createProduct

PUT → updateProduct

DELETE → deleteProduct (soft delete)

## 2: HTTP Status Codes (5 used)

200 OK → success responses

201 Created → on new product creation

400 Bad Request → for invalid input or ID

404 Not Found → for missing products or bad IDs

500 Server Error → internal error

## 3:Stateless & Database Connected
The API stores data in a MongoDB Atlas database via Mongoose. Restarting the server does not affect stored data.

### 4: SEO and Accessibility

To ensure accessibility, I used semantic HTML and Chakra UI components that support keyboard navigation and screen readers. I added clear labels to all form inputs and used aria-required attributes to indicate mandatory fields. Color contrast was improved using high-contrast combinations for readability. 
For SEO, I used react-helmet to set the page title and meta description to help search engines understand the content of the page.

### 5: Tracking
To track usage statistics Google Tag Manager is integrated in the Application which is tracking Page Load and Navigation at the moment. The tracking can be extended to track user actions like Button and Link clicks.  

## 6: Security (OWASP)
This project mitigates several common web vulnerabilities as identified by OWASP:

1. A03:2021 Injection
   This project is secured from SQL/code injection attacks using ExpressJs and MongoDB which prevents execution of SQL or other code on the Web Server and in the Database Engine.

2. A06:2021 Vulnerable and Outdated Components    
   All the frontend libraries and packages are latest and has no vulnerable or outdated dependencies. This can be confirmed by running the `npm audit` which returns `found 0 vulnerabilities` message


