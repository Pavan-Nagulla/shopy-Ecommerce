# Shopy E-Commerce

**Shopy E-Commerce** is a modern online shopping platform built with a **React** frontend and a **Spring Boot** backend. It allows users to browse products, add them to their cart, and securely complete purchases using **Razorpay** for payment processing.

This README will guide you through setting up the development environment, installing necessary tools, and running the project locally.

---

## Table of Contents

1. [Setting Up Your Development Environment](#setting-up-your-development-environment)
2. [Backend Development with Spring Boot](#backend-development-with-spring-boot)
3. [Frontend Development with React](#frontend-development-with-react)
4. [Styling with MUI and Tailwind CSS](#styling-with-mui-and-tailwind-css)
5. [Connecting Frontend and Backend](#connecting-frontend-and-backend)
6. [Deployment and Hosting](#deployment-and-hosting)
7. [Bonus Topics](#bonus-topics)
8. [Tech Stack](#tech-stack)
9. [How to Run the Project](#how-to-run-the-project)

---

## 1. Setting Up Your Development Environment

### Tools Required

To get started with the project, you need to install the following tools:

1. **Node.js and npm**: To run the React frontend.
   - [Download Node.js](https://nodejs.org/)
   
2. **Java Development Kit (JDK)**: To run the Spring Boot backend.
   - [Download JDK](https://adoptopenjdk.net/)

3. **MySQL Database**: For storing user and product data.
   - [Download MySQL](https://dev.mysql.com/downloads/installer/)

4. **IDE/Editor**: Recommended IDEs are:
   - [Visual Studio Code (VSCode)](https://code.visualstudio.com/)
   - [IntelliJ IDEA](https://www.jetbrains.com/idea/)

5. **Git**: Version control for managing project code.
   - [Download Git](https://git-scm.com/)

---

## 2. Backend Development with Spring Boot

The backend is built with **Spring Boot** and follows a RESTful architecture to handle API requests.

### Key Features:
- User authentication and authorization using **Spring Security**.
- Product listings, shopping cart management, and order processing.
- MySQL database integration for data storage.

### Steps to Set Up the Backend:
1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/shopy-ecommerce.git
   cd shopy-ecommerce/backend

Install the required dependencies using Maven:
mvn install
Configure the MySQL database by editing the application.properties file in the src/main/resources folder:
spring.datasource.url=jdbc:mysql://localhost:3306/shopy_db
spring.datasource.username=root
spring.datasource.password=yourpassword
Run the Spring Boot application:
mvn spring-boot:run
The backend will be available at http://localhost:8080.
3. Frontend Development with React

The frontend of the website is built with React and provides a dynamic, responsive user interface for customers.

Key Features:
Product catalog with search functionality.
Shopping cart and checkout system.
User authentication.
Steps to Set Up the Frontend:
Navigate to the frontend directory:
cd shopy-ecommerce/frontend
Install the necessary dependencies using npm:
npm install
Start the React development server:
npm start
The frontend will be available at http://localhost:3000.
4. Styling with MUI and Tailwind CSS

Material UI (MUI)
We use MUI (Material-UI) to design modern and user-friendly UI components. Material-UI provides a set of pre-built components that help us maintain a consistent design language.

MUI Website: https://mui.com/
Tailwind CSS
We use Tailwind CSS for utility-first styling, which allows us to apply CSS classes directly in the HTML/JSX without writing separate stylesheets.

Tailwind CSS Documentation: https://tailwindcss.com/
5. Connecting Frontend and Backend

CORS Configuration:
To allow the React frontend to communicate with the Spring Boot backend, we need to configure CORS (Cross-Origin Resource Sharing) on the backend.

In BackendApplication.java, add:

@CrossOrigin(origins = "http://localhost:3000")
@SpringBootApplication
public class BackendApplication {
    public static void main(String[] args) {
        SpringApplication.run(BackendApplication.class, args);
    }
}
This allows the frontend to make requests to the backend from http://localhost:3000.

6. Deployment and Hosting

Preparing for Production:
Frontend Deployment:
Build the React application for production:
npm run build
Backend Deployment:
Package the Spring Boot application as a .jar file:
mvn clean package
Deploy both frontend and backend to a hosting service of your choice, such as:
Heroku
Netlify (for frontend)
AWS
Example Deployment Steps for Heroku:
Install Heroku CLI: Heroku CLI
Login to Heroku:
heroku login
Deploy your app:
git push heroku master
7. Bonus Topics

Integrating Payment Gateways: The website integrates Razorpay for payment processing. Follow the Razorpay documentation to set up your payment gateway.
Advanced Features: Future enhancements include:
User reviews and ratings for products.
Personalized product recommendations using machine learning.
8. Tech Stack

Frontend:
Framework: React
UI Libraries: Tailwind CSS, Material-UI (MUI)
State Management: Redux
Authentication: JWT (JSON Web Tokens)
Routing: React Router Dom
Backend:
Framework: Spring Boot
Security: Spring Security
Database: MySQL
Payment Gateway: Razorpay
9. How to Run the Project

Step 1: Clone the Repository
git clone https://github.com/yourusername/shopy-ecommerce.git
cd shopy-ecommerce
Step 2: Set Up the Backend
Navigate to the backend directory.
Install Maven dependencies:
mvn install
Configure MySQL database credentials in application.properties.
Run the backend:
mvn spring-boot:run
Step 3: Set Up the Frontend
Navigate to the frontend directory.
Install npm dependencies:
npm install
Start the React development server:
npm start
Step 4: Access the Website
Frontend: http://localhost:3000
Backend: http://localhost:8080
