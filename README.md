# Cinema Website

A modern, responsive cinema website built with Vue.js and Vite. Features a sleek dark theme with interactive movie library, contact form, and mobile-optimized design.


## ✨ Features

- **Responsive Design**: Fully optimized for desktop, tablet, and mobile devices
- **Interactive Movie Library**: Search, view, and remove movies from your collection
- **Smooth Navigation**: Fixed navigation bar with smooth scrolling to sections
- **Contact Form**: Functional contact form with validation
- **Modern UI**: Clean, dark theme with hover effects and animations
- **Mobile-First**: Optimized mobile experience with hamburger menu
- **Component-Based**: Modular Vue.js components for maintainability

## 🚀 Tech Stack

- **Frontend Framework**: Vue.js 3
- **Build Tool**: Vite
- **Styling**: CSS3 with Flexbox and Grid
- **Icons**: Custom SVG icons
- **Maps**: Google Maps integration
- **Responsive**: Mobile-first responsive design

## 📦 Installation

### Prerequisites

- Node.js (version 16 or higher)
- npm or yarn package manager

### Setup

1. **Clone the repository**
   \`\`\`bash
   git clone https://github.com/ashen8981/cinema-website.git
   cd cinema-website
   \`\`\`

2. **Install dependencies**
   \`\`\`bash
   npm install
   # or
   yarn install
   \`\`\`

3. **Start development server**
   \`\`\`bash
   npm run dev
   # or
   yarn dev
   \`\`\`

4. **Open your browser**
   Navigate to `http://localhost:5173`

## 🎯 Usage

### Navigation
- Use the navigation bar to jump to different sections
- Mobile users can access the hamburger menu for navigation

### Movie Library
- **Search**: Use the search bar to filter movies by title
- **Remove**: Click the × button on any movie card to remove it
- **Responsive Grid**: Movies automatically adjust to screen size

### Contact Form
- Fill out all required fields (marked with *)
- Accept terms and conditions to submit
- Form includes validation for email format

### Mobile Experience
- Optimized layouts for mobile and tablet devices
- Touch-friendly interface elements
- Responsive typography and spacing

## 🛠️ Development

### Available Scripts

\`\`\`bash
# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
\`\`\`

### Adding New Components

1. Create component file in `src/components/`
2. Create corresponding CSS file in `src/assets/css/`
3. Import and register in parent component
4. Follow existing naming conventions

### Styling Guidelines

- Use CSS custom properties for consistent theming
- Follow mobile-first responsive design approach
- Maintain consistent spacing using rem units
- Use semantic class names

## 📱 Responsive Breakpoints

- **Mobile**: `max-width: 480px`
- **Tablet**: `max-width: 768px`
- **Desktop**: `min-width: 769px`

## 🎨 Color Palette

- **Primary Background**: `#000` (Black)
- **Secondary Background**: `#111` (Dark Gray)
- **Card Background**: `#222` (Medium Gray)
- **Input Background**: `#333` (Light Gray)
- **Accent Color**: `#f39c12` (Orange)
- **Text Primary**: `#fff` (White)
- **Text Secondary**: `#ccc` (Light Gray)
- **Text Muted**: `#666` (Gray)

## 🌟 Key Features Explained

### Movie Library
- Dynamic search functionality
- Responsive grid layout
- Interactive movie cards with hover effects
- Remove functionality with smooth animations

### Contact Form
- Form validation
- Required field indicators
- Terms and conditions checkbox
- Responsive form layout

### Navigation
- Fixed position navbar
- Smooth scrolling to sections
- Mobile hamburger menu
- Active state indicators

## 🚀 Deployment

### Build for Production

\`\`\`bash
npm run build
\`\`\`

The built files will be in the `dist/` directory, ready for deployment to any static hosting service.

### Deployment Options

- **Vercel**: Connect your GitHub repository for automatic deployments
- **Netlify**: Drag and drop the `dist` folder or connect via Git
- **GitHub Pages**: Use GitHub Actions for automated deployment
- **Firebase Hosting**: Deploy using Firebase CLI

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 🙏 Acknowledgments

- **Icons**: Custom SVG icons
- **Maps**: Google Maps Platform

## 📞 Support

If you have any questions or need help with setup, please open an issue in the repository.

---

**Built with ❤️ using Vue.js and Vite**
