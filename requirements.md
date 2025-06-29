### 1. 🧑‍💼 User Authentication
🔹 Functional Requirements
Users must be able to register using their name, email, and password.

Users must be able to log in using email and password.

Passwords must be securely hashed.

A unique session or token is issued upon login.

🔸 Technical Requirements
API Endpoints

POST /api/auth/register

POST /api/auth/login

Input/Output Specifications

POST /api/auth/register
Input (JSON):

json
Copy
Edit
{
  "first_name": "Sara",
  "last_name": "Sattar",
  "email": "sara@example.com",
  "password": "MyStrongPass123"
}
Output (Success):

json
Copy
Edit
{
  "message": "User registered successfully",
  "user_id": "uuid"
}
Validation Rules:

Email must be valid and unique.

Password must be at least 8 characters.

### 2. 🏠 Property Management
🔹 Functional Requirements
Hosts can add, edit, and delete properties.

Hosts can set pricing and descriptions.

Properties are linked to the host user account.

🔸 Technical Requirements
API Endpoints

POST /api/properties/ (Add Property)

PUT /api/properties/{id} (Edit Property)

DELETE /api/properties/{id} (Delete Property)

Input Example for Add Property

json
Copy
Edit
{
  "host_id": "uuid",
  "name": "Cozy Studio in Medina",
  "description": "A peaceful studio near city center.",
  "location": "Marrakech",
  "pricepernight": 70.00
}
Validation Rules

Price must be positive.

Description must not be empty.

Only users with role=host can perform this.

Performance Criteria

API should respond in <500ms.

Should handle 1000 concurrent requests.

### 3. 📆 Booking System
🔹 Functional Requirements
Users can book available properties.

Booking requires selecting dates and paying the total price.

Status should be updated on booking actions.

🔸 Technical Requirements
API Endpoints

POST /api/bookings/

GET /api/bookings/{user_id}

Input Example for Booking

json
Copy
Edit
{
  "user_id": "uuid",
  "property_id": "uuid",
  "start_date": "2025-07-15",
  "end_date": "2025-07-17"
}
Output

json
Copy
Edit
{
  "message": "Booking created successfully",
  "booking_id": "uuid",
  "total_price": 140.00
}
Validation Rules

Start date must be before end date.

Property must be available for those dates.

User must be authenticated.