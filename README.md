# Voyage Guardian - AI-Powered Travel Planning App

A modern, AI-powered travel planning application built with React, TypeScript, and Supabase. Plan your perfect trip with personalized itineraries, weather forecasts, currency conversion, and intelligent chat support.

## ✨ Features

- **AI-Powered Itinerary Generation** - Get personalized travel plans based on your preferences
- **Smart Authentication** - Secure login with email/password and Google OAuth
- **Weather Integration** - Real-time weather forecasts for your destination
- **Currency Converter** - Support for 45+ global currencies with live exchange rates
- **Intelligent Chat Support** - AI travel assistant to help with planning
- **Trip Management** - Save, edit, and manage your travel itineraries
- **Responsive Design** - Beautiful UI that works on all devices
- **Hidden Gems Discovery** - Find local secrets beyond typical tourist spots

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- npm or yarn
- Supabase account (for authentication and database)

### Installation

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd voyage-guardian
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Fill in your API keys in the `.env` file:
   ```env
   # Supabase Configuration
   VITE_SUPABASE_URL=https://your-project-id.supabase.co
   VITE_SUPABASE_ANON_KEY=your_supabase_anon_key_here

   # API Keys (Optional - app works with fallback data)
   VITE_OPENAI_API_KEY=your_openai_api_key
   VITE_WEATHER_API_KEY=your_weather_api_key
   VITE_EXCHANGE_API_KEY=your_exchange_api_key
   ```

4. **Start development server**
   ```bash
   npm run dev
   ```

## 🌐 Deployment

### Deploy to Vercel (Recommended)

1. **Connect your repository to Vercel**
   - Go to [Vercel Dashboard](https://vercel.com/dashboard)
   - Click "New Project" and import your repository

2. **Configure environment variables**
   - In your Vercel project settings, add all environment variables from your `.env` file
   - Make sure to use the exact same variable names

3. **Deploy**
   - Vercel will automatically deploy on every push to main branch
   - Your app will be available at `https://your-project.vercel.app`

### Manual Build

```bash
npm run build
npm run preview
```

## 🔧 Configuration

### Supabase Setup

1. **Create a new project** at [Supabase](https://app.supabase.com)
2. **Get your credentials** from Settings > API
3. **Run database migrations** - The app includes pre-built migrations
4. **Enable Google OAuth** (optional) in Authentication > Providers
5. **Update your `.env` file** with the credentials

### API Keys Setup

The app works with fallback data even without API keys, but for full functionality:

- **OpenAI**: Required for AI itinerary generation and chat
- **Weather API**: Required for real weather forecasts (OpenWeatherMap)
- **Exchange Rate API**: Required for live currency rates

## 📱 Usage

1. **Sign up/Login** - Create an account or sign in
2. **Plan Your Trip** - Enter destination, dates, budget, and preferences
3. **Get Your Itinerary** - AI generates a personalized travel plan
4. **Save Your Trip** - Store itineraries for future reference
5. **Explore Features** - Check weather, convert currencies, chat with AI assistant
6. **Manage Trips** - View, edit, and delete saved trips

## 🛠️ Tech Stack

### Frontend
- **React 18** - Modern React with hooks
- **TypeScript** - Type-safe development
- **Tailwind CSS** - Utility-first styling
- **Framer Motion** - Smooth animations
- **Lucide React** - Beautiful icons
- **Vite** - Fast build tool

### Backend & Services
- **Supabase** - Authentication and database
- **PostgreSQL** - Relational database with RLS
- **OpenAI API** - AI-powered itinerary generation
- **OpenWeatherMap** - Weather forecasts
- **ExchangeRate-API** - Currency conversion

### Deployment
- **Vercel** - Serverless deployment
- **Edge Functions** - API endpoints

## 🏗️ Project Structure

```
src/
├── components/           # React components
│   ├── Auth/            # Authentication components
│   ├── Chat/            # Chat support
│   ├── Dashboard/       # Trip dashboard and widgets
│   ├── Landing/         # Landing page
│   ├── Layout/          # Layout components
│   └── Planning/        # Trip planning forms
├── hooks/               # Custom React hooks
├── lib/                 # Library configurations
├── services/            # API services
├── types/               # TypeScript type definitions
└── main.tsx            # Application entry point

supabase/
└── migrations/          # Database migrations
```

## 🎨 Design Features

- **Modern Gradient Backgrounds** - Beautiful visual design
- **Glass Morphism Effects** - Contemporary UI elements
- **Smooth Animations** - Framer Motion powered transitions
- **Responsive Design** - Works on all devices
- **Accessible Components** - WCAG compliant
- **Dark/Light Theme Support** - User preference based

## 🔒 Security Features

- **Row Level Security (RLS)** - Database-level security
- **JWT Authentication** - Secure token-based auth
- **Environment Variables** - Secure API key management
- **CORS Protection** - Cross-origin request security
- **Input Validation** - Client and server-side validation

## 📊 Database Schema

### Tables
- **profiles** - User profile information
- **saved_trips** - User's saved trip itineraries
- **trips** - Main trip planning data
- **days** - Individual days within trips
- **activities** - Activities for each day

### Security
- All tables have Row Level Security enabled
- Users can only access their own data
- Proper foreign key relationships

## 🚨 Error Handling

- **Graceful API Failures** - Fallback data when APIs are unavailable
- **Form Validation** - Client-side validation with helpful messages
- **Network Error Recovery** - Automatic retries and fallbacks
- **User-Friendly Messages** - Clear error communication

## 🔄 Development History

### Phase 1: Foundation (Initial Setup)
- ✅ React + TypeScript + Vite setup
- ✅ Tailwind CSS configuration
- ✅ Basic component structure
- ✅ Landing page design

### Phase 2: Authentication (Supabase Integration)
- ✅ Supabase client setup
- ✅ Authentication modal
- ✅ User registration and login
- ✅ Google OAuth integration
- ✅ Password reset functionality

### Phase 3: Trip Planning (Core Features)
- ✅ Trip planning form
- ✅ Multi-step form validation
- ✅ Travel style selection
- ✅ Interest-based preferences

### Phase 4: AI Integration (OpenAI)
- ✅ OpenAI API integration
- ✅ Itinerary generation
- ✅ Chat support system
- ✅ Rate limiting and error handling

### Phase 5: Dashboard (Trip Management)
- ✅ Trip dashboard design
- ✅ Itinerary display
- ✅ Weather widget
- ✅ Currency converter
- ✅ Save trip functionality

### Phase 6: Data Persistence (Database)
- ✅ Database schema design
- ✅ Trip saving and loading
- ✅ User trip management
- ✅ Trip editing and deletion

### Phase 7: Polish & Optimization
- ✅ Responsive design improvements
- ✅ Animation enhancements
- ✅ Error handling improvements
- ✅ Performance optimizations

### Phase 8: Deployment (Production Ready)
- ✅ Vercel deployment configuration
- ✅ Environment variable management
- ✅ Build optimization
- ✅ Production error handling

## 🐛 Known Issues & Solutions

### Fixed Issues
- ✅ **Rate Limiting** - Implemented proper API rate limiting
- ✅ **NaN Calculations** - Added safe number conversions
- ✅ **Form Validation** - Comprehensive input validation
- ✅ **Mobile Responsiveness** - Fixed layout issues
- ✅ **API Error Handling** - Graceful fallbacks

### Current Status
- 🟢 **Stable** - Production ready
- 🟢 **Responsive** - Works on all devices
- 🟢 **Secure** - Proper authentication and data protection
- 🟢 **Fast** - Optimized performance

## 📈 Performance Optimizations

- **Code Splitting** - Lazy loading of components
- **Image Optimization** - Responsive images with proper sizing
- **Bundle Optimization** - Vendor chunk separation
- **Caching** - Proper HTTP caching headers
- **Minification** - Production build optimization

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🆘 Support

If you encounter any issues:

1. **Check the documentation** above
2. **Review environment variables** - Make sure all required variables are set
3. **Check API keys** - Ensure all API keys are valid and have proper permissions
4. **Open an issue** - Provide detailed error information

## 🙏 Acknowledgments

- **Supabase** - For the amazing backend-as-a-service platform
- **OpenAI** - For the powerful AI capabilities
- **Vercel** - For seamless deployment
- **Tailwind CSS** - For the utility-first CSS framework
- **Framer Motion** - For beautiful animations

---

**Built with ❤️ using React, TypeScript, and modern web technologies.**

**Live Demo**: [Your Vercel URL]
**Repository**: [Your GitHub URL]