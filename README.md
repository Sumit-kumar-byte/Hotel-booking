# Airbnb 

This is a full-stack Airbnb built using modern web technologies. It includes a React-based frontend and a Node.js/Express backend with a MySQL database.

## Features

- *Home Page*: Displays a list of properties with images, ratings, and pricing.
- *Search Functionality*: Compact and full search bar for filtering properties by location, dates, and guests.
- *Category Bar*: Scrollable category bar for filtering properties by type (e.g., Farms, Amazing Views, Treehouses).
- *Property Grid*: Displays properties in a grid layout with details like location, cost, and ratings.
- *Map View*: Interactive map showing property locations with markers and popups.
- *Favorites*: Mark properties as favorites and save them to local storage.
- *Filter Modal*: Advanced filtering options for cities and price range.
- *Responsive Design*: Optimized for both desktop and mobile devices.
- *404 Page*: Custom-designed page for handling undefined routes.
- *Header and Footer*: Navigation links and additional information.
- *Authentication*:
  - *Login*: Users can log in using their email and password.
  - *Logout*: Users can securely log out of their account.
- *Profile Management*: Users can view, update, and save changes to their profile information.
- *Watchlist*: Users can add properties to their watchlist and view them later.
- *Hotel Booking*: Users can book hotels by selecting check-in and check-out dates and view their booking history.

## Backend Technologies

- *Node.js*: JavaScript runtime for building the backend.
- *Express.js*: Web framework for creating RESTful APIs.
- *MySQL*: Relational database for storing application data.
- *Sequelize*: ORM for interacting with the MySQL database.
- *JWT*: For user authentication and authorization.
- *bcrypt.js*: For password hashing.

## Folder Structure


Airbnb/
├── frontend/        # Frontend application
│   ├── public/      # Static assets (e.g., images, icons)
│   ├── src/
│   │   ├── components/  # Reusable components
│   │   ├── pages/       # Page components (e.g., HomePage, NotFoundPage)
│   │   ├── App.tsx      # Main application component
│   │   ├── index.tsx    # Entry point
│   │   ├── styles/      # Global styles
│   │   └── utils/       # Utility functions
│   ├── package.json     # Frontend dependencies
│   └── README.md        # Frontend documentation
├── backend/         # Backend application
│   ├── src/
│   │   ├── controllers/ # Business logic for routes
│   │   ├── models/      # Database models (MySQL)
│   │   ├── routes/      # API routes
│   │   ├── config/      # Configuration files (e.g., database connection)
│   │   └── server.js    # Server entry point
│   ├── .env            # Environment variables
│   ├── package.json     # Backend dependencies
│   └── README.md        # Backend documentation


## Installation and Setup

Follow these steps to clone and run the project locally:

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager
- MySQL (v8 or higher)

### Clone the Repository

bash
git clone https://github.com/your-username/airbnb-clone.git
cd airbnb-clone


### Install Frontend Dependencies

bash
cd frontend
npm install
# or
yarn install


### Start the Frontend Development Server

bash
npm start
# or
yarn start


The application will be available at http://localhost:3000.

### Install Backend Dependencies

bash
cd backend
npm install


### Configure the Database

1. Create a MySQL database using the database/schema.sql file.
2. Add sample data using the database/seed.sql file.
3. Create a .env file in the backend folder with the following content:

env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=airbnb_clone
JWT_SECRET=your_jwt_secret
PORT=5000


### Start the Backend Server

bash
cd backend
npm start


The backend server will run on http://localhost:5000.

### Build for Production

To create a production build for the frontend, run:

bash
cd frontend
npm run build
# or
yarn build


The build files will be generated in the build directory.

### Run Tests

To run tests (if implemented):

bash
npm test
# or
yarn test


## Database Tables

The following tables are created in the MySQL database:

- *users*: Stores user information (e.g., name, email, password).
- *properties*: Stores property details (e.g., title, location, price).
- *wishlist*: Stores user wishlists for properties.
- *bookings*: Stores booking details (e.g., check-in, check-out dates).
- *notifications*: Stores user notifications.

## API Endpoints

- *Authentication*
  - POST /api/register: Register a new user.
  - POST /api/login: Log in a user and return a JWT token.
  - POST /api/logout: Log out the user (client-side token removal).
- *Profile*
  - GET /api/profile: Fetch the user's profile information (requires authentication).
  - PUT /api/profile: Update the user's profile information (requires authentication).
- *Properties*
  - GET /api/properties: Fetch all properties.
  - POST /api/properties: Add a new property (requires authentication).
- *Watchlist*
  - POST /api/wishlist: Add a property to the watchlist (requires authentication).
  - GET /api/wishlist: Fetch the user's watchlist (requires authentication).
  - DELETE /api/wishlist/:id: Remove a property from the watchlist (requires authentication).
- *Bookings*
  - POST /api/bookings: Create a new booking (requires authentication).
  - GET /api/bookings: Fetch the user's bookings (requires authentication).
  - DELETE /api/bookings/:id: Cancel a booking (requires authentication).
- *Notifications*
  - GET /api/notifications: Fetch user notifications (requires authentication).

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License. See the LICENSE file for details.