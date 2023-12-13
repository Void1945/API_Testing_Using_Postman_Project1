INTRODUCTION

This documentation provides comprehensive information on the API testing suite designed for restful-booker.herokuapp.com. 
The suite includes a Postman collection and environment tailored to streamline API testing for diverse functionalities associated with Booking management. 
The API enables various operations, such as fetching existing bookings, creating new bookings, retrieving created bookings, generating tokens for authorization, updating bookings, dynamically fetching updated bookings, and deleting bookings. Additionally, the suite supports importing datasets from CSV files for creating bookings and successfully retrieving them.

Please note that the purpose of this API testing suite is to ensure the robustness and reliability of the restful-booker.herokuapp.com API by thoroughly examining its functionalities and ensuring seamless interactions with the Booking management system.

SUMMARY

The purpose of this API testing suite is to ensure the robustness and reliability of the restful-booker.herokuapp.com API by thoroughly examining its functionalities and ensuring seamless interactions with the Hotel Booking management system.


API REQUESTS

Generating Token for Authorization

Endpoint: https://restful-booker.herokuapp.com/auth

Method: POST

Description: Generates a token for authorization, enabling secure access to restricted endpoints.


Creating a New Booking

Endpoint: {{baseUrl}}/booking

Method: POST

Description: Creates a new booking with the specified parameters.

Updating Booking

Endpoint: {{baseUrl}}/booking/{{booking_id}}

Method: PUT

Description: Updates the details of an existing booking identified by the provided bookingId.

Updating Booking

Endpoint: {{baseUrl}}/booking/{{booking_id}}

Method: PUT

Description: Updates the details of an existing booking identified by the provided bookingId.

Deleting Booking

Endpoint: {{baseUrl}}/booking/{{booking_id}}

Method: DELETE

Description: Deletes the booking associated with the specified bookingId.


Retrieving Created Booking

Endpoint: {{baseUrl}}/booking/{{booking_id}}

Method: GET

Description: Retrieves details of the booking created using the specified bookingId.



Test Script

pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

Authorization Token

