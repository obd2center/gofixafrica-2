# AutoAfrica Marketplace

A comprehensive automotive services and parts marketplace platform for Africa, connecting customers with service providers, parts traders, and ECU/diagnostic file services across multiple African countries.

## 🌍 Overview

AutoAfrica Marketplace is a digital platform designed to revolutionize the automotive industry in Africa by providing:
- **Service Marketplace**: Connect with verified automotive service providers
- **Parts Trading**: Buy and sell automotive parts with RFQ (Request for Quote) system
- **ECU & Diagnostic Services**: Upload, download, and manage ECU files and diagnostic services
- **Multi-Region Support**: Subdomain-based country routing (ke.autoafrica.com, ng.autoafrica.com, etc.)

## ✨ Features

### Core Marketplace
- Provider onboarding and verification
- Service listings with ratings and reviews
- Booking and inquiry management
- Parts marketplace with stock tracking
- RFQ system for custom part requests
- ECU file upload/download with order tracking

### Localization & Multi-Region
- Support for 5+ African countries (Kenya, Nigeria, South Africa, Ghana, Tanzania)
- Multi-language interface (English, Swahili, French)
- Region-specific currency display
- Localized payment methods

### User Management
- JWT-based authentication
- Role-based access control (Customer, Service Provider, Parts Trader, Admin)
- Social login support
- OTP verification ready

### Payment Integration
- Flutterwave integration ready
- Paystack support ready
- M-Pesa integration ready
- Webhook handling for payment confirmations

## 🛠️ Tech Stack

- **Frontend**: Next.js 14, React 18, TypeScript
- **Styling**: Tailwind CSS, shadcn/ui components
- **Authentication**: NextAuth.js with JWT
- **Database**: PostgreSQL with Prisma ORM
- **File Storage**: AWS S3 integration
- **Animations**: Framer Motion

## 📋 Prerequisites

- Node.js 18+ 
- PostgreSQL 14+
- Yarn package manager
- AWS account (for S3 storage)

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/obd2center/gofixafrica-2.git
cd gofixafrica-2
```

### 2. Install dependencies

```bash
cd nextjs_space
yarn install
```

### 3. Set up environment variables

Create a `.env` file in the `nextjs_space` directory:

```env
# Database
DATABASE_URL="postgresql://user:password@localhost:5432/autoafrica"

# NextAuth
NEXTAUTH_SECRET="your-secret-key-here"
NEXTAUTH_URL="http://localhost:3000"

# AWS S3
AWS_BUCKET_NAME="your-bucket-name"
AWS_FOLDER_PREFIX="autoafrica/"
AWS_REGION="us-east-1"
AWS_ACCESS_KEY_ID="your-access-key"
AWS_SECRET_ACCESS_KEY="your-secret-key"

# Payment Gateways (Optional)
FLUTTERWAVE_SECRET_KEY="your-flutterwave-key"
PAYSTACK_SECRET_KEY="your-paystack-key"
```

### 4. Set up the database

```bash
# Generate Prisma client
yarn prisma generate

# Push schema to database
yarn prisma db push

# Seed the database with sample data
yarn prisma db seed
```

### 5. Run the development server

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 👤 Test Credentials

After seeding the database, you can log in with:

- **Email**: john@doe.com
- **Password**: johndoe123

## 📁 Project Structure

```
nextjs_space/
├── app/                    # Next.js app directory
│   ├── api/               # API routes
│   ├── auth/              # Authentication pages
│   ├── dashboard/         # User dashboard
│   ├── services/          # Service marketplace
│   ├── parts/             # Parts marketplace
│   └── ecu/               # ECU services
├── components/            # React components
│   ├── ui/               # UI components
│   └── navbar.tsx        # Navigation
├── lib/                   # Utility functions
│   ├── auth-options.ts   # NextAuth configuration
│   ├── db.ts             # Database client
│   ├── s3.ts             # S3 file handling
│   └── region.ts         # Multi-region support
├── prisma/               # Database schema
│   └── schema.prisma     # Prisma schema
└── public/               # Static assets
```

## 🗄️ Database Schema

The application uses 18+ database models including:
- Users, Regions, ServiceProviders
- Services, ServiceBookings, ServiceCategories
- PartsTraders, Products, RFQs
- ECUServices, ECUOrders
- Reviews, Payments, and more

## 🌐 Multi-Region Support

The platform supports multiple African countries with:
- Subdomain-based routing (e.g., ke.autoafrica.com for Kenya)
- Region-specific currencies and payment methods
- Localized content and language support

## 🔐 Security

- JWT-based authentication
- Password hashing with bcrypt
- Protected API routes
- Role-based access control
- Secure file upload with S3

## 📱 Mobile Support

- Fully responsive design
- Mobile-first approach
- PWA capabilities ready
- Optimized for slow connections

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License.

## 📧 Contact

For questions or support, please contact the development team.

---

**Built with ❤️ for Africa's automotive industry**
