# Car_Parking_Application
This Car Parking Apllication is a Spring Boot microservice-based application that allows users to register, view available parking slots, and book them. It supports booking tracking and slot management with clean REST APIs.

## Technologies Used
Java 17+
Spring Boot
Spring Data JPA
MySQL
OpenAPI/Swagger
Feign Client (to communicate with User Service)

## Modules
1. Entities
ParkingSlot: Represents individual parking slots.
Booking: Stores booking records linked to users and slots.

3. DTOs
BookingRequest: Request body to book a slot.
UserDTO: Used to retrieve user info from user-management-service.

4. Repositories
ParkingSlotRepository
BookingRepository

4. Services
ParkingService: Create, book, release, and check slots.
BookingService: Save and fetch booking data.

5. Controllers
ParkingController: Handles slot-related endpoints.
BookingController: Handles booking-related endpoints.

6. Feign Client
UserServiceClient: Retrieves user info from the User Service.

## How to Run
1. Update application.properties with your DB credentials.
2. Build and run the project:
      ./mvnw spring-boot:run
3. Access Swagger UI:
      http://localhost:8082/swagger-ui/index.html

## ENDPOINTS:

### parking-controller
1. POST /api/parking/create
2. GET /api/parking/available
3. GET /api/parking/all

### booking-controller
POST /api/bookings

### user-controller
1. POST /api/users/register
2. GET /api/users/{username}
