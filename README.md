# VaultIQ Inventory Management - Frontend

A premium React-based frontend for the VaultIQ inventory management system. Built with a modern Black & Gold design, this dashboard provides a seamless interface for product browsing, order management, and admin analytics.

## ✨ Features

- **User Authentication**: Secure login and registration with JWT tokens
- **Role-Based Access Control**: Different dashboards for regular users and admins
- **Product Browsing**: Browse and search products with detailed information
- **Order Management**: Create, view, and track orders
- **Admin Dashboard**: Analytics overview with real-time statistics
- **Admin Controls**: Product management, user management, and order tracking
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile
- **Premium UI**: Black & Gold color scheme with smooth animations

## 🚀 Getting Started

### Prerequisites
- Node.js 16+
- npm or yarn
- Backend API running

### Installation

1. Clone the repository
```bash
git clone https://github.com/D-Audit/inventory-management.git
cd inventory-management/frontend
```

2. Install dependencies
```bash
npm install
```

3. Set up environment variables
Create a `.env.local` file:
```env
REACT_APP_API_URL=http://localhost:7000/api
```

4. Start development server
```bash
npm start
```

The app will run at `http://localhost:3000`

## 📁 Project Structure

```
frontend/
├── src/
│   ├── api/
│   │   └── index.js                # API fetch helper with JWT injection
│   ├── context/
│   │   └── AuthContext.jsx         # Global auth state
│   ├── components/
│   │   ├── Login.jsx               # Login page
│   │   ├── Register.jsx            # Register page
│   │   ├── Navbar.jsx              # Navigation sidebar
│   │   ├── Dashboard.jsx           # User dashboard
│   │   ├── Products.jsx            # Product browsing
│   │   ├── AddProduct.jsx          # Add/edit product modal
│   │   ├── AdminDashboard.jsx      # Admin analytics
│   │   ├── AdminProducts.jsx       # Admin product management
│   │   ├── AdminOrders.jsx         # Admin order management
│   │   ├── AdminUsers.jsx          # Admin user management
│   │   ├── ProtectedRoute.jsx      # Route guard
│   │   └── MyOrders.jsx            # User's orders
│   ├── App.js                       # Main app entry
│   ├── App.css                      # Global styles
│   └── index.js                     # React entry point
├── .env.local                       # Environment variables
└── package.json
```

## 🎨 Design System

### Colors
- **Background**: #0a0a0a
- **Surface**: #111111
- **Gold**: #c9a84c
- **Gold Light**: #e8c96d
- **Success**: #52a96e
- **Danger**: #e05252
- **Warning**: #d4943a

### Typography
- **Display Font**: Playfair Display (headings)
- **Body Font**: Inter (body text)

## 🔐 Authentication

The app uses JWT (JSON Web Tokens) for authentication:

1. User registers or logs in
2. Server returns JWT token
3. Token stored in localStorage
4. Token sent with every API request in Authorization header
5. Backend validates token on protected routes

## 👥 User Roles

### Regular User
- View all products
- Browse product catalog
- Place orders
- View their own orders
- Cancel pending orders

### Admin User
- Access admin dashboard
- View all statistics and analytics
- Create, edit, and delete products
- View and manage all orders
- Update order status
- Manage user accounts
- View top products and sales trends

## 🛠️ Technologies

- **React 18**: UI framework
- **Context API**: State management
- **Fetch API**: HTTP requests
- **CSS3**: Styling with animations
- **React Router**: Navigation (if used)

## 📱 Responsive Design

- **Mobile** (0-600px): Single column layout, optimized touch targets
- **Tablet** (600-960px): Two-column layout
- **Desktop** (960px+): Full-featured multi-column layout

## 🔄 API Integration

The frontend communicates with the backend API:

### Authentication
- POST `/api/auth/register` - Register new account
- POST `/api/auth/login` - Login
- GET `/api/auth/users` - Get all users (admin only)

### Products
- GET `/api/products` - Get all products
- POST `/api/products` - Create product (admin)
- PUT `/api/products/:id` - Update product (admin)
- DELETE `/api/products/:id` - Delete product (admin)

### Orders
- GET `/api/orders` - Get user's orders
- POST `/api/orders` - Create new order
- PUT `/api/orders/:id` - Update order status (admin)
- DELETE `/api/orders/:id` - Delete order (admin)

## 🚀 Deployment

### Build for Production
```bash
npm run build
```

### Deploy to Vercel
```bash
npm install -g vercel
vercel
```

### Deploy to Netlify
1. Connect GitHub repository
2. Set build command: `npm run build`
3. Set publish directory: `build`

## 🎯 Best Practices

- Always verify token before API calls
- Handle errors gracefully with user feedback
- Validate form inputs before submission
- Protect admin routes with role checks
- Keep sensitive data in backend only
- Use environment variables for API endpoints

## 🐛 Troubleshooting

### API Connection Issues
- Verify backend is running
- Check `REACT_APP_API_URL` environment variable
- Check browser console for CORS errors

### Authentication Issues
- Clear localStorage and try again
- Verify JWT token is valid
- Check if token is being sent in headers

### Styling Issues
- Clear browser cache
- Restart development server
- Check CSS file is imported correctly

## 📚 Resources

- [React Documentation](https://react.dev)
- [Context API Guide](https://react.dev/reference/react/useContext)
- [MDN Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)

## 📝 License

This project is available under the MIT License.

## 👨‍💻 Author

**KAYIRANGA Jesus**
- GitHub: [@D-Audit](https://github.com/D-Audit)
- Role: Software Engineer & Full Stack Developer

---

Built with premium design and seamless user experience.
