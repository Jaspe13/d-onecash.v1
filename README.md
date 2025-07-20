# D-OneCash

A comprehensive digital finance platform that enables advanced blockchain-integrated financial services with a focus on flexible cryptocurrency lending and secure asset management.

System Architecture
1. Microservices Architecture:
   


<img width="840" height="863" alt="Captura de pantalla 2025-07-20 140830" src="https://github.com/user-attachments/assets/3a0bab8d-b33d-4fbb-af3c-d61adbf400c4" />


The architecture follows a modern microservices pattern with clear separation of concerns:

- **Frontend Layer**: Multi-platform interfaces (Web, Mobile, Admin, Merchant)
- **API Gateway**: Centralized routing, authentication, and rate limiting
- **Microservices**: Domain-specific services with dedicated responsibilities
- **Data Layer**: Distributed storage with XRPL integration and analytics

## 🚀 Features

- **Digital Wallet**: Send and receive USD with QR code support
- **Cryptocurrency Loans**: Use BTC as collateral for USDC loans
- **Contact Management**: Easy contact system for frequent transfers
- **Business Payments**: Terminal for contactless and QR payments
- **Virtual Cards**: Manage virtual debit cards
- **Inheritance System**: Digital asset inheritance planning
- **Multi-language Support**: English interface
- **Real-time Updates**: Live transaction tracking

## 🛠 Tech Stack

- **Frontend**: React + TypeScript + Vite
- **Backend**: Express.js + Node.js
- **Database**: PostgreSQL with Drizzle ORM
- **UI Components**: Radix UI + Tailwind CSS
- **Authentication**: Session-based with Replit Auth
- **State Management**: TanStack Query

## 📋 Prerequisites

- Node.js 18+ 
- PostgreSQL database
- npm or yarn package manager

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/d-onecash.git
cd d-onecash
```

2. Install dependencies:
```bash
npm install
```

3. Set up environment variables:
```bash
cp .env.example .env
```

4. Configure your environment variables in `.env`:
```
DATABASE_URL=your_postgresql_connection_string
SESSION_SECRET=your_session_secret_key
REPL_ID=your_replit_app_id
ISSUER_URL=https://replit.com/oidc
```

5. Set up the database:
```bash
npm run db:push
```

6. Start the development server:
```bash
npm run dev
```

The application will be available at `http://localhost:5000`

## 🗄️ Database Schema

The application uses PostgreSQL with the following main tables:
- `users` - User accounts and profile information
- `wallets` - User wallet balances and currency info
- `transactions` - Transaction history and details
- `contacts` - User contact management
- `qr_codes` - Generated QR codes for payments
- `heirs` - Inheritance system beneficiaries
- `sessions` - User session management

## 💳 Loan System

- **Collateral**: Bitcoin (BTC) up to 1 BTC maximum
- **Interest Rate**: 6% annual
- **Loan Duration**: 1-5 years
- **Loan-to-Value**: Up to 50% of BTC value
- **Early Payment Fee**: 1% for early cancellation
- **Late Payment Policy**: 1% fee + partial BTC liquidation

## 🏢 Business Features

- Payment terminal for in-store transactions
- Contactless payment support
- QR code payment processing
- Transaction commission: 1% + $0.25 (web), $0.25 (in-store)

## 🎨 UI/UX

- Responsive design for mobile, tablet, and desktop
- Dark/Light theme support
- Green and black D-OneCash branding
- Intuitive navigation with hamburger menu
- Accessible components with screen reader support

## 📱 Mobile Optimization

- Mobile-first responsive design
- Touch-friendly interface
- Optimized QR code scanning
- Collapsible sections for space efficiency

## 🔐 Security

- Session-based authentication
- Secure API endpoints
- Input validation with Zod schemas
- CSRF protection
- Database connection pooling

## 🚀 Deployment

The application is optimized for deployment on platforms like:
- Replit (recommended)
- Vercel
- Netlify
- Railway
- DigitalOcean

For production deployment:
1. Set `NODE_ENV=production`
2. Configure production database
3. Set secure session secrets
4. Enable HTTPS
5. Configure domain settings

## 📝 API Endpoints

### User Management
- `GET /api/user/:id` - Get user profile
- `GET /api/wallet/:id` - Get wallet balance

### Transactions
- `GET /api/transactions/:userId` - Get transaction history
- `POST /api/transactions/send` - Send money
- `POST /api/transactions/loan` - Create loan transaction

### Contacts
- `GET /api/contacts/:userId` - Get user contacts
- `POST /api/contacts` - Add new contact
- `PUT /api/contacts/:id` - Update contact
- `DELETE /api/contacts/:id` - Delete contact

### QR Codes
- `GET /api/qr-codes/:userId` - Get user QR codes
- `POST /api/qr-codes` - Generate new QR code

### Inheritance
- `GET /api/heirs/:userId` - Get inheritance beneficiaries
- `POST /api/heirs` - Add heir
- `PUT /api/heirs/:id` - Update heir
- `DELETE /api/heirs/:id` - Remove heir

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

For support and questions:
- Create an issue in this repository
- Contact the development team
- Check the documentation

## 🎯 Roadmap

- [ ] Real cryptocurrency integration
- [ ] Multi-currency support
- [ ] Advanced trading features
- [ ] Mobile app development
- [ ] Enhanced security features
- [ ] Integration with external payment providers

---

**D-OneCash** - Bridging Web2 experience with Web3 technology for seamless digital finance.
