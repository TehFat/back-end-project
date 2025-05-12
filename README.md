# Prodcut Management
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


## Tracking & Privacy

I have implemented Google Tag Manager (GTM) to track key user interactions within the application, such as:

Viewing the product list

Adding new products

Editing product details

Deleting products

This tracking helps me better understand how the app is used so I can improve usability and overall user experience.

### Why I use GTM:
I use GTM to:
- Gain insights into which parts of the app users engage with the most
- Identify potential usability issues or bugs
- Improve the design and performance of the application

### How I respect user privacy:
- I do not collect any personally identifiable information (PII)
- All data tracked is anonymous and used only for internal analysis
- GTM is configured to only track essential events (no marketing or third-party ad scripts)
- I follow GDPR principles by avoiding tracking methods that store personal data or use cookies for advertising
- Users are made aware of tracking through this documentation and a clear description in the application if applicable




## 6: Security (OWASP)
This project mitigates several common web vulnerabilities as identified by OWASP:

1. A03:2021 Injection
   This project is secured from SQL/code injection attacks using ExpressJs and MongoDB which prevents execution of SQL or other code on the Web Server and in the Database Engine.

2. A06:2021 Vulnerable and Outdated Components    
   All the frontend libraries and packages are latest and has no vulnerable or outdated dependencies. This can be confirmed by running the `npm audit` which returns `found 0 vulnerabilities` message




