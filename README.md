# Social Market App - Technical README

## Overview
The **Social Market App** is a platform designed to enhance social engagement by allowing subscribers to boost their status, views, and reach through credit-based purchases or collaborative activities. Users can buy credits to access premium services or participate in group engagements that promote organic interactions.

## Features
- **User Authentication**: Secure login and registration using OAuth and email verification.
- **Credit-Based Transactions**: Users can purchase credits to unlock engagement services.
- **Subscription Plans**: Monthly and yearly plans for accessing collaborative activities.
- **Engagement Services**:
  - Boosting social media views, likes, and shares.
  - Increasing profile engagement through collaborative tasks.
  - Sponsored content promotions.
- **Marketplace**: A hub where users can exchange credits for services.
- **Analytics Dashboard**: Users can track their engagement progress.
- **Referral System**: Users earn credits by inviting new subscribers.
- **Payment Gateway Integration**: Supports multiple payment methods.

## Technical Stack
- **Frontend**: Laravel Livewire/Volt
- **Backend**: Laravel (PHP)
- **Database**: MySQL / PostgreSQL
- **Authentication**: Laravel Passport / Firebase Auth
- **Real-time Features**: WebSockets / Pusher
- **Payments**: PayStack / Stripe / PayPal API
- **Hosting**: AWS / DigitalOcean

## Architecture
The Social Market App follows a **microservices-inspired** architecture with the following core components:

### 1. **User Service**
Handles authentication, profile management, and subscription tracking.

### 2. **Credits & Transactions Service**
Manages credit purchases, transactions, and payment processing.

### 3. **Engagement Service**
Responsible for executing engagement-related tasks, such as scheduling boosts and collaborative activities.

### 4. **Marketplace Service**
Facilitates the exchange of credits for engagement services.

### 5. **Analytics Service**
Collects and displays data on user engagement and progress.

## API Endpoints
### Authentication
- `POST /api/register` – User registration
- `POST /api/login` – User login
- `POST /api/logout` – Logout user

### Credits & Transactions
- `GET /api/credits` – Get user credit balance
- `POST /api/credits/buy` – Purchase credits
- `POST /api/transactions/history` – View transaction history

### Engagement Services
- `POST /api/engagement/boost` – Request a social media boost
- `POST /api/engagement/collaborate` – Join a collaborative engagement
- `GET /api/engagement/status` – Check engagement progress

## Deployment
### **Steps to Deploy**
1. Clone the repository:  
   ```bash
   git clone https://github.com/bhioux/socialmarket.git
   ```
2. Install backend dependencies:
   ```bash
   cd backend && composer install
   ```
3. Set up environment variables:
   ```bash
   cp .env.example .env
   ```
4. Run migrations:
   ```bash
   php artisan migrate
   ```
5. Start the backend server:
   ```bash
   php artisan serve
   ```
6. Install frontend dependencies:
   ```bash
   cd frontend && npm install
   ```
7. Start the frontend:
   ```bash
   npm run dev
   ```

## Security Measures
- **JWT Authentication** for API security
- **Rate Limiting** to prevent abuse
- **Data Encryption** for user-sensitive data
- **Role-Based Access Control (RBAC)** to manage user permissions

## Future Enhancements
- AI-powered engagement recommendations
- Smart credit rewards for active users
- Integration with additional social media platforms
- Decentralized engagement verification using blockchain

## Contributing
Contributions are welcome! Please submit pull requests or open an issue for discussion.

## License
This project is licensed under the MIT License.

