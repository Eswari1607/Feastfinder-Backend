**FeastFinder Backend**
The backend for FeastFinder handles the server-side operations, including database management, API endpoints, user authentication, and business logic. Built with Express.js, this repository supports all the main functionalities of the FeastFinder website.

**Features**
User Authentication: Secure user login and registration.

Restaurant Management: CRUD operations for restaurant data.

Reservation Management: Handling user reservations, modifications, and cancellations.

Review Management: Allowing users to leave reviews and administrators to respond.

Admin Features: Admin capabilities for managing reservations and reviews.

**Prerequisites**
Node.js

Express.js

MongoDB 

**Getting Started**
Installation
Clone the repository:

bash
git clone <backend_repository_url>
Navigate to the project directory:

bash
cd feastfinder-backend
Install dependencies:

bash
npm install
Running the Application
For development:

bash
npm start
The server will start running on http://localhost:5000.

env
PORT=5000
DATABASE_URL=mongodb+srv://Eshu:kamala1607@cluster0.px4ov.mongodb.net/?retryWrites=true&w=majority&appName=Cluster0
JWT_SECRET=dsafjfsahsadkjdfkdsasac36hdssbd37.ddsahdddf

**API Endpoints**
Authentication
POST /api/auth/signup: User signup.

POST /api/auth/signin: User signin.

Restaurants
GET /api/restaurants: Get all restaurant data.

GET /api/restaurants/:city: Get restaurants by city.

GET /api/restaurants/:city/:id: Get a restaurant by city and id.

POST /api/restaurants: Add a new restaurant.

PUT /api/restaurants/:id: Update restaurant details.

DELETE /api/restaurants/:id: Delete a restaurant.

Reservations
POST /api/reservations: Make a new reservation.

GET /api/reservations: Get a list of reservations.

PUT /api/reservations/:id: Modify a reservation.

DELETE /api/reservations/:id: Cancel a reservation.

Reviews
POST /api/reviews: Leave a new review.

GET /api/reviews: Get a list of reviews.

PUT /api/reviews/:id: Update a review.

DELETE /api/reviews/:id: Delete a review.

POST /api/admin/reply: Submit a reply to a review.

POST /api/reviews/submit-review: Submit a review for a specific restaurant.

GET /api/reviews/get-reviews/:hotelId: Fetch reviews for a specific hotel.

PUT /api/reviews/edit-review/:reviewId: Edit a review.

Bookings
POST /api/bookings/create-booking: Create a new booking.

GET /api/bookings/:userId: Fetch bookings by user ID.

PUT /api/bookings/cancelBooking/:bookingId: Cancel a booking.

GET /api/bookings/all-bookings: Fetch all bookings for admin.

PUT /api/bookings/updateBooking/:bookingId: Update booking status.

PUT /api/bookings/editBooking/:bookingId: Edit booking details.

Admin Guide
Accepting/Rejecting Reservations
Send a PUT request to /api/admin/reservations/:id/accept or /api/admin/reservations/:id/reject with the reservation ID.

Receive a confirmation of the action.

Responding to Reviews
Send a POST request to /api/admin/reviews/:id/respond with the review ID and response text.

Receive a confirmation of the response being posted.

Submitting a Reply to a Review
Send a POST request to /api/admin/reply with the reviewId and adminReply.

Receive a confirmation of the reply being added.

Creating and Managing Bookings
Creating a Booking
Send a POST request to /api/bookings/create-booking with the booking details.

Receive a confirmation of the booking being created.

Fetching Bookings by User ID
Send a GET request to /api/bookings/:userId with the user ID.

Receive the list of bookings for the specified user.

Canceling a Booking
Send a PUT request to /api/bookings/cancelBooking/:bookingId with the booking ID.

Receive a confirmation of the booking being canceled.

Fetching All Bookings (Admin)
Send a GET request to /api/bookings/all-bookings to fetch all bookings.

Receive the list of all bookings.

Updating Booking Status
Send a PUT request to /api/bookings/updateBooking/:bookingId with the booking ID and status.

Receive a confirmation of the booking status being updated.

Editing Booking Details
Send a PUT request to /api/bookings/editBooking/:bookingId with the booking ID and updated details.

Receive a confirmation of the booking being updated.

Review Management
Submitting a Review
Send a POST request to /api/reviews/submit-review with the review details.

Receive a confirmation of the review being submitted.

How to Contribute
Fork the Repository: Click on the "Fork" button at the top right of the repository page to create a copy of the repository under your GitHub account.

Clone the Forked Repository:

bash
git clone <forked_repository_url>
cd feastfinder-backend
Create a New Branch:

bash
git checkout -b feature/your-feature-name
Make Your Changes: Implement your feature or fix.

Commit Your Changes:

bash
git add .
git commit -m "Add description of changes"
Push to Your Forked Repository:

bash
git push origin feature/your-feature-name
Submit a Pull Request: Go to the original repository and submit a pull request from your forked repository's branch.

Guidelines
Follow the existing code style and structure.

Write clear, concise commit messages.

Test your changes thoroughly before submitting.

If you add new features, please provide documentation and update the README as necessary.

Reporting Issues
If you find a bug or have a feature request, please create an issue on the repository's issue tracker.

Contact
Gmail:eswarikamala1607@gmail.com
