# ShqipZone - Albanian Lyrics Translation Platform

🌍 **Platforma më e madhe për përkthimin e këngëve në shqip**

ShqipZone is a comprehensive web platform dedicated to translating foreign songs into Albanian. Built with modern technologies, it provides a collaborative environment for translators, music enthusiasts, and Albanian language learners.

## 🚀 Features

### Core Features
- **Song Management**: Add, edit, and manage songs from various languages
- **Translation System**: Create and manage Albanian translations with different types (literal, poetic, adapted)
- **User Authentication**: Secure registration and login system
- **Community Features**: Comments, likes, corrections, and user profiles
- **Translation Requests**: Request translations for specific songs
- **Search & Filter**: Advanced search functionality with multiple filters
- **Admin Panel**: Comprehensive admin dashboard for content moderation

### Technical Features
- **Modern UI/UX**: Beautiful, responsive design with Tailwind CSS
- **Real-time Updates**: Live notifications and updates
- **Mobile Responsive**: Optimized for all device sizes
- **SEO Optimized**: Meta tags, structured data, and performance optimized
- **Security**: JWT authentication, input validation, rate limiting
- **Performance**: Optimized queries, caching, and lazy loading

## 🛠️ Tech Stack

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **JWT** - Authentication
- **bcryptjs** - Password hashing
- **Joi** - Input validation
- **Helmet** - Security middleware

### Frontend
- **React 18** - UI library
- **React Router** - Client-side routing
- **React Query** - Data fetching and caching
- **Tailwind CSS** - Styling framework
- **Lucide React** - Icon library
- **Framer Motion** - Animations
- **React Hook Form** - Form management

## 📋 Prerequisites

Before running this project, make sure you have the following installed:

- **Node.js** (v16 or higher)
- **npm** or **yarn**
- **MongoDB** (local installation or MongoDB Atlas)

## 🚀 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/shqipzone.git
cd shqipzone
```

### 2. Install Dependencies

```bash
# Install backend dependencies
npm install

# Install frontend dependencies
cd client
npm install
cd ..
```

### 3. Environment Configuration

Create a `.env` file in the root directory:

```bash
cp env.example .env
```

Edit the `.env` file with your configuration:

```env
# Server Configuration
PORT=5000
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/shqipzone

# JWT Configuration
JWT_SECRET=your-super-secret-jwt-key-change-this-in-production

# Client Configuration
CLIENT_URL=http://localhost:3000
```

### 4. Database Setup

Make sure MongoDB is running on your system. If using MongoDB Atlas, update the `MONGODB_URI` in your `.env` file.

### 5. Run the Application

#### Development Mode (Recommended)

```bash
# Run both backend and frontend concurrently
npm run dev
```

This will start:
- Backend server on `http://localhost:5000`
- Frontend development server on `http://localhost:3000`

#### Production Mode

```bash
# Build the frontend
npm run build

# Start the production server
npm start
```

## 📁 Project Structure

```
shqipzone/
├── server/                 # Backend code
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   ├── middleware/        # Custom middleware
│   └── index.js           # Server entry point
├── client/                # Frontend code
│   ├── public/            # Static files
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── pages/         # Page components
│   │   ├── contexts/      # React contexts
│   │   ├── services/      # API services
│   │   └── index.js       # App entry point
│   └── package.json
├── package.json           # Root package.json
└── README.md
```

## 🔧 Configuration

### Backend Configuration

The backend can be configured through environment variables:

- `PORT`: Server port (default: 5000)
- `MONGODB_URI`: MongoDB connection string
- `JWT_SECRET`: Secret key for JWT tokens
- `NODE_ENV`: Environment (development/production)

### Frontend Configuration

The frontend can be configured through environment variables:

- `REACT_APP_API_URL`: Backend API URL (default: http://localhost:5000/api)

## 🎯 Usage

### For Users

1. **Register/Login**: Create an account or log in to access all features
2. **Browse Songs**: Explore songs from various languages and genres
3. **View Translations**: Read Albanian translations with original lyrics
4. **Request Translations**: Submit requests for songs that need translation
5. **Contribute**: Add comments, corrections, and feedback

### For Translators

1. **Create Translations**: Add Albanian translations for songs
2. **Choose Translation Type**: Select between literal, poetic, or adapted translations
3. **Add Notes**: Include translation notes and context
4. **Get Feedback**: Receive comments and corrections from the community

### For Administrators

1. **Content Moderation**: Approve/reject songs and translations
2. **User Management**: Manage user accounts and roles
3. **Statistics**: View platform analytics and insights
4. **System Maintenance**: Monitor and maintain the platform

## 🔒 Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: Bcrypt password encryption
- **Input Validation**: Comprehensive input validation with Joi
- **Rate Limiting**: API rate limiting to prevent abuse
- **CORS Protection**: Cross-origin resource sharing protection
- **Helmet Security**: Security headers and middleware

## 📊 API Endpoints

### Authentication
- `POST /api/auth/register` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/me` - Get current user
- `PUT /api/auth/profile` - Update profile

### Songs
- `GET /api/songs` - Get all songs
- `GET /api/songs/:id` - Get song by ID
- `POST /api/songs` - Create new song
- `PUT /api/songs/:id` - Update song
- `DELETE /api/songs/:id` - Delete song

### Translations
- `GET /api/translations` - Get all translations
- `GET /api/translations/:id` - Get translation by ID
- `POST /api/translations` - Create new translation
- `PUT /api/translations/:id` - Update translation
- `POST /api/translations/:id/verify` - Verify translation

### Translation Requests
- `GET /api/requests` - Get all requests
- `POST /api/requests` - Create new request
- `PUT /api/requests/:id` - Update request
- `POST /api/requests/:id/assign` - Assign request to translator

## 🧪 Testing

```bash
# Run backend tests
npm test

# Run frontend tests
cd client
npm test
```

## 🚀 Deployment

### Backend Deployment

1. Set up a MongoDB database (MongoDB Atlas recommended)
2. Configure environment variables
3. Deploy to your preferred platform (Heroku, Vercel, AWS, etc.)

### Frontend Deployment

1. Build the application: `npm run build`
2. Deploy the `build` folder to your hosting platform
3. Configure environment variables for production

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -am 'Add feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **LyricsTranslate.com** - Inspiration for the platform concept
- **Albanian Language Community** - For supporting Albanian language preservation
- **Open Source Community** - For the amazing tools and libraries used

## 📞 Support

If you have any questions or need support:

- **Email**: support@shqipzone.com
- **Issues**: [GitHub Issues](https://github.com/yourusername/shqipzone/issues)
- **Documentation**: [Wiki](https://github.com/yourusername/shqipzone/wiki)

## 🌟 Roadmap

- [ ] Mobile app development
- [ ] Advanced search filters
- [ ] Translation memory system
- [ ] Audio pronunciation guides
- [ ] Social media integration
- [ ] Translation quality scoring
- [ ] Multi-language support for the platform
- [ ] API for third-party integrations

---

**ShqipZone** - Preserving and promoting the Albanian language through music translation 🎵🇦🇱 