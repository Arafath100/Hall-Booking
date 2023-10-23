# Hall Booking API

 This is a Node.js and Express-based API for managing a hall booking application. It allows you to create rooms, book rooms, list rooms with bookings, and more.

# API Documentation:

 For detailed documentation of the API endpoints and how to use them, please refer to our [API Documentation](https://documenter.getpostman.com/view/30678354/2s9YRCWBX5).

## Table of Contents
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Creating a Room](#creating-a-room)
  - [Booking a Room](#booking-a-room)
  - [Listing Rooms with Bookings](#listing-rooms-with-bookings)
  - [Listing Customers with Bookings](#listing-customers-with-bookings)
  - [Customer Booking History](#customer-booking-history)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)

## Getting Started:

### Prerequisites
- Node.js and npm installed on your machine.

### Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/Arafath100/Hall-Booking.git
   cd hall-booking

2. Install dependencies:
   ```bash
   npm install body-parser express

3. Start the server:
   ```bash
   node index.js

## Usage:

### Creating a Room

#### To create a room, make a POST request to /create-room with the following JSON data:

     ```bash
     {
       "roomNumber": "101",
       "seatsAvailable": 50,
       "amenities": Wifi, AC,
       "pricePerHour": $100
     }

### Booking a Room

#### To book a room, make a POST request to /book-room with the following JSON data:

     {
       "roomId": "101",
       "customerName": "John Doe",
       "date": "2023-10-23",
       "startTime": "10:00:00 AM",
       "endTime": "12:00:00 PM"
     }

### Listing Rooms with Bookings

  To list all rooms with their bookings, make a GET request to `/rooms-with-bookings`.

### Listing Customers with Bookings

  To list all customers with their bookings, make a GET request to `/customers-with-bookings`.

### Customer Booking History

  To list how many times a customer has booked a room with details, make a GET request to `/customer-booking-history/:customerName`, replacing `:customerName` with the actual customer's name.

## API Endpoints:

• `POST /create-room:` Create a room. <br/>
• `POST /book-room:` Book a room. <br/>
• `GET /rooms:` List all rooms. <br/>
• `GET /rooms-with-bookings:` List all rooms with their bookings. <br/>
• `GET /customers-with-bookings:` List all customers with their bookings. <br/>
• `GET /customer-booking-history/:customerName:` List a customer's booking history. <br/>

## Contributing:

 Contributions are welcome! If you want to improve this project, feel free to open issues or submit pull requests.

## License:
  This project is licensed under the MIT License.
