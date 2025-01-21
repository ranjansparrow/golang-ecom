# golang-ecom
First GoLang Ecommerce Project


# E-commerce Project with React & Go

A simple e-commerce application built with React frontend and Go backend, featuring Stripe integration for payments.

## Features

- Product listing and display
- Shopping cart functionality
- Secure payment processing with Stripe
- Customer information collection
- Responsive design

## Tech Stack

### Frontend
- React
- Stripe Elements for payment UI
- CSS for styling

### Backend
- Go (Golang)
- Stripe Go SDK for payment processing

## Prerequisites

Before running this project, make sure you have the following installed:
- Node.js (v14 or higher)
- Go (v1.16 or higher)
- Stripe account and API keys

## Installation & Setup

### Backend Setup

1. Clone the repository
```bash
git clone [your-repository-url]
cd [project-directory]/backend
```

2. Install Go dependencies
```bash
go mod tidy
```

3. Create a `.env` file in the backend directory
```plaintext
STRIPE_SECRET_KEY=your_stripe_secret_key_here
```

4. Start the Go server
```bash
go run main.go
```
The server will start on `localhost:4242`

### Frontend Setup

1. Navigate to the frontend directory
```bash
cd [project-directory]/frontend
```

2. Install dependencies
```bash
npm install
```

3. Create a `.env` file in the frontend directory
```plaintext
REACT_APP_STRIPE_PUBLISHABLE_KEY=your_stripe_publishable_key_here
```

4. Start the React development server
```bash
npm start
```
The application will open in your browser at `localhost:3000`

## API Endpoints

### `/create-payment-intent` (POST)
Creates a Stripe PaymentIntent for processing payments.

Request body:
```json
{
  "product_id": "Forever Pants",
  "first_name": "John",
  "last_name": "Doe",
  "address1": "123 Street",
  "address2": "Apt 4",
  "city": "Boston",
  "state": "MA",
  "zip": "02101",
  "country": "US"
}
```

Response:
```json
{
  "clientSecret": "pi_xxx_secret_xxx"
}
```

## Available Products

- Forever Pants ($250.00)
- Forever Shirt ($150.00)
- Forever Shorts ($300.00)

## Environment Variables

### Backend
- `STRIPE_SECRET_KEY`: Your Stripe secret key

### Frontend
- `REACT_APP_STRIPE_PUBLISHABLE_KEY`: Your Stripe publishable key

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

## Acknowledgments

- [Stripe Documentation](https://stripe.com/docs)
- [React Documentation](https://reactjs.org/)
- [Go Documentation](https://golang.org/doc/)