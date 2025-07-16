# D-OneCash - Digital Finance Platform

A comprehensive digital finance platform that enables advanced blockchain-integrated financial services with a focus on flexible cryptocurrency lending and secure asset management.

## 🚀 Features

- **Digital Wallet**: Secure USD balance management
- **Money Transfers**: Send money via email, phone, or username
- **QR Code Payments**: Generate and scan QR codes for payments
- **Contact Management**: Add and manage payment contacts
- **Cryptocurrency Loans**: BTC collateral lending system
- **Virtual Cards**: Secure virtual debit card management
- **Business Terminal**: Payment processing for businesses
- **Inheritance System**: Secure fund inheritance management
- **Multi-language Support**: English interface
- **Mobile Responsive**: Optimized for all devices

## 🛠️ Tech Stack

- **Frontend**: React + TypeScript + Vite
- **Backend**: Node.js + Express
- **Database**: PostgreSQL (optional, includes in-memory storage)
- **UI Components**: Radix UI + Tailwind CSS
- **State Management**: TanStack Query
- **Forms**: React Hook Form + Zod validation

## 📱 App Sections

1. **Wallet** - View balance and transaction history
2. **Send Money** - Transfer funds to contacts
3. **QR Codes** - Generate payment QR codes
4. **Contacts** - Manage payment contacts
5. **Loans** - BTC collateral lending
6. **Cards** - Virtual card management
7. **Business** - Payment terminal
8. **Heirs** - Inheritance settings
9. **Settings** - Profile and app settings
10. **Help & Support** - Customer support

## 🚀 Quick Start

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start development server:**
   ```bash
   npm run dev
   ```

3. **Open your browser:**
   Navigate to `http://localhost:5000`

## 📦 Deployment

### Railway Deployment
1. Connect your GitHub repository to Railway
2. Set environment variables if using database
3. Deploy automatically

### Replit Deployment
1. Click "Deploy" in Replit
2. Select "Autoscale"
3. Get your public URL

## 🔧 Environment Variables

```env
NODE_ENV=production
DATABASE_URL=postgresql://... # Optional
SESSION_SECRET=your-secret-key # If using authentication
```

## 📁 Project Structure

```
d-onecash/
├── client/              # React frontend
│   ├── src/
│   │   ├── components/  # UI components
│   │   ├── pages/       # App pages
│   │   ├── hooks/       # Custom hooks
│   │   └── lib/         # Utilities
├── server/              # Express backend
│   ├── routes.ts        # API routes
│   ├── storage.ts       # Data storage
│   └── index.ts         # Server entry
├── shared/              # Shared types
│   └── schema.ts        # Database schema
└── public/              # Static assets
```

## 🎨 Design System

- **Colors**: Green and black theme matching D-OneCash branding
- **Typography**: Modern, clean fonts
- **Icons**: Lucide React icons
- **Layout**: Mobile-first responsive design

## 📄 License

MIT License - see LICENSE file for details.

## 👥 Support

For support and questions, use the in-app Help & Support section or contact the development team.

---

**D-OneCash** - Making digital finance accessible to everyone.