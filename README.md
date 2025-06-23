🚀 Product Management System (Spring Boot + Spring Security + Swagger)
This is a simple Product Management System built with Spring Boot, Spring Security (Basic Authentication), Swagger for API documentation, and MySQL for data storage.

🛠️ Features
✔️ RESTful API for managing products
✔️ Product entity with fields: pid, pname, price, review
✔️ Global Exception Handling
✔️ Spring Security with Basic Authentication
✔️ Swagger API Documentation for easy testing
✔️ MySQL Integration

📦 Tech Stack
Java 17+

Spring Boot

Spring Security (Basic Auth)

Spring Data JPA

MySQL Database

Swagger 3 (OpenAPI)

Maven

🗄️ Product Structure
Product entity contains:

Field	Type	Description
pid	Long	Auto-generated Product ID
pname	String	Product Name
price	Double	Product Price
review	String	Product Review/Description

🔒 Spring Security
Basic Authentication is enabled.

You must provide username and password to access protected endpoints.

Default credentials (can be modified in application.properties):

applictation properties
--------------------------
spring.security.user.name=admin
spring.security.user.password=admin123


📑 Swagger UI - API Testing
After running the application, access Swagger UI at:

👉 http://localhost:8080/swagger-ui/index.html

Use Swagger to test API endpoints easily. Authentication popup will appear; enter the credentials.


⚙️ How to Run the Application
1. Clone the Repository
git clone https://github.com/your-username/product-management-system.git

2. Configure Database
Make sure MySQL is running. Update your application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/productdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
Create the database manually:


Application runs at: http://localhost:8080

🎯 Available API Endpoints
Method	Endpoint	Description	Authentication Required
GET	/products	Get all products	✅ Yes
GET	/products/{id}	Get product by ID	✅ Yes
POST	/products	Create new product	✅ Yes
PUT	/products/{id}	Update existing product	✅ Yes
DELETE	/products/{id}	Delete product by ID	✅ Yes

⚠️ Exception Handling
If a product is not found, a custom exception message is returned.

Global exception handling is implemented under exception package.

👨‍💻 Example Product JSON for Testing

{
  "pname": "iPhone 15 Pro",
  "price": 134999.99,
  "review": "Premium smartphone with advanced features"
}
📝 Notes
Swagger endpoints like /swagger-ui/** and /v3/api-docs/** are publicly accessible.

All /products/** endpoints require authentication.

📢 Contributing
Feel free to fork, enhance, or raise issues for improvements.

💡 Future Enhancements
JWT-based authentication
Role-based access control
Unit & Integration tests

📞 Contact
For questions, reach me at: gdk26102000@gmail.com
