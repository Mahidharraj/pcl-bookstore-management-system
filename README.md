# PCL Bookstore Management System

A comprehensive bookstore management system with e-commerce capabilities built using Node.js, Express, MongoDB, and HTML/CSS/JavaScript.

## Features

- **User Authentication & Authorization**
  - User registration and login
  - JWT-based authentication
  - Role-based access control (User/Admin)
  - Password reset functionality
  - Email verification

- **Book Management**
  - Browse books by category
  - Search and filter books
  - View detailed book information
  - Admin: Add, edit, delete books
  - Stock management
  - Featured books, bestsellers, new arrivals

- **Shopping Cart**
  - Add/remove items
  - Update quantities
  - Apply coupon codes
  - Cart persistence

- **Order Management**
  - Place orders
  - Order tracking
  - Order history
  - Order cancellation
  - Invoice generation

- **Payment Integration**
  - Multiple payment methods
  - Secure payment processing
  - Payment verification

## Tech Stack

### Backend
- Node.js
- Express.js
- MongoDB with Mongoose
- JWT for authentication
- Bcrypt for password hashing

### Frontend
- HTML5
- CSS3
- JavaScript (Vanilla)
- Responsive design

## Installation

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (v4.4 or higher)
- npm or yarn

### Setup Instructions

1. **Clone the repository**
```bash
cd "pcl project codes"
```

2. **Install dependencies**
```bash
npm install
```

3. **Set up environment variables**
```bash
# Copy the example env file
copy .env.example .env

# Edit .env file with your configuration
notepad .env
```

4. **Start MongoDB**
Make sure MongoDB is running on your system:
```bash
# For Windows
mongod
```

5. **Run the application**
```bash
# Development mode
npm run dev

# Production mode
npm start
```

The application will be available at `http://localhost:5000`

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `GET /api/auth/me` - Get current user
- `POST /api/auth/logout` - Logout user
- `POST /api/auth/forgotpassword` - Request password reset
- `PUT /api/auth/resetpassword/:token` - Reset password

### Books
- `GET /api/books` - Get all books
- `GET /api/books/:id` - Get single book
- `GET /api/books/featured` - Get featured books
- `GET /api/books/bestsellers` - Get bestsellers
- `GET /api/books/new-arrivals` - Get new arrivals
- `POST /api/books` - Add new book (Admin)
- `PUT /api/books/:id` - Update book (Admin)
- `DELETE /api/books/:id` - Delete book (Admin)

### Cart
- `GET /api/cart` - Get user cart
- `POST /api/cart/add` - Add item to cart
- `PUT /api/cart/update` - Update cart item
- `DELETE /api/cart/remove/:bookId` - Remove item
- `DELETE /api/cart/clear` - Clear cart
- `POST /api/cart/coupon` - Apply coupon

### Orders
- `GET /api/orders` - Get user orders
- `GET /api/orders/:id` - Get order details
- `POST /api/orders` - Create order
- `PUT /api/orders/:id/cancel` - Cancel order

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update profile

## Project Structure

```
pcl-project-codes/
├── backend/
│   ├── config/         # Database configuration
│   ├── controllers/    # Route controllers
│   ├── middleware/     # Custom middleware
│   ├── models/         # Mongoose models
│   ├── routes/         # API routes
│   ├── utils/          # Utility functions
│   └── public/         # Static files
├── images/             # Frontend images
├── index.html          # Homepage
├── books.html          # Books page
├── cart.html           # Shopping cart
├── payment.html        # Payment page
├── About.html          # About page
├── Contact.html        # Contact page
├── Services.html       # Services page
├── main login.html     # Login page
├── style.css           # Main stylesheet
├── server.js           # Express server
├── package.json        # Dependencies
├── .env.example        # Environment variables example
└── README.md           # Documentation
```

## Security Features

- Password hashing with bcrypt
- JWT token authentication
- Input validation
- SQL injection prevention
- XSS protection
- CORS configuration
- Environment variables for sensitive data

## Development

### Running in Development Mode
```bash
npm run dev
```
This will start the server with nodemon for auto-reloading on file changes.

### Database Seeding
To populate the database with sample data, you can create a seed script or manually add books through the admin panel.

## Deployment

### Production Considerations
1. Set `NODE_ENV=production` in environment variables
2. Use a process manager like PM2
3. Set up MongoDB Atlas for cloud database
4. Configure proper CORS settings
5. Use HTTPS in production
6. Set strong JWT secret keys

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the ISC License.

## Support

For support, email your-email@example.com or create an issue in the repository.

## Acknowledgments

- Node.js and Express.js communities
- MongoDB documentation
- All contributors and testers
