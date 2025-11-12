# Yash Zode - Portfolio Website

A modern, responsive portfolio website integrated with Cal.com for seamless meeting scheduling.

## 🌟 Features

- **Modern Design**: Clean, professional, and responsive design that works on all devices
- **Cal.com Integration**: Direct booking functionality embedded in the portfolio
- **Smooth Animations**: Engaging scroll animations and transitions
- **Responsive Layout**: Mobile-first design that adapts to all screen sizes
- **SEO Optimized**: Proper meta tags and semantic HTML
- **Fast Loading**: Optimized for performance

## 📁 Project Structure

```
.
├── index.html          # Main HTML file
├── styles.css          # All styles and responsive design
├── script.js           # JavaScript for interactivity
├── assets/             # Images, icons, and media files
│   ├── images/         # Portfolio images
│   └── icons/          # Icon files
└── README.md           # This file
```

## 🚀 Getting Started

### Prerequisites

- A GitHub account
- A Cal.com account (sign up at https://cal.com)
- Basic knowledge of Git

### Setup Instructions

1. **Clone or Download this Repository**
   ```bash
   git clone https://github.com/YashZode/yashzode.github.io.git
   cd yashzode.github.io
   ```

2. **Update Cal.com Username**
   - Open `index.html`
   - Find the Cal.com script initialization (around line 15-20)
   - Replace `"yashzode"` with your actual Cal.com username if different
   - Also update the `calLink` in the inline embed (around line 400)

3. **Customize Your Content**
   - Update personal information in `index.html`:
     - Name, title, and description in the hero section
     - Skills and expertise levels
     - Projects and portfolio items
     - Contact information
     - Social media links
   - Update `styles.css` to match your brand colors (CSS variables at the top)

4. **Add Your Images** (Optional)
   - Add your profile picture to `assets/images/`
   - Update the avatar placeholder in the hero section
   - Add project screenshots to `assets/images/`

5. **Deploy to GitHub Pages**
   - Push your changes to the `main` branch
   - Go to your repository settings on GitHub
   - Navigate to "Pages" in the left sidebar
   - Select "main" branch as source
   - Your site will be live at `https://yashzode.github.io`

## 🔧 Cal.com Integration

This portfolio includes Cal.com integration in multiple ways:

1. **Inline Embed**: Full calendar view in the booking section
2. **Button Triggers**: Quick booking buttons throughout the site
3. **Floating Widget**: Can be added for always-visible booking

### Setting Up Cal.com

1. **Create a Cal.com Account**
   - Sign up at https://cal.com
   - Complete your profile setup
   - Create event types (15min, 30min, 60min meetings)

2. **Get Your Cal.com Username**
   - Your username is in your Cal.com profile URL
   - Example: `https://app.cal.com/yashzode` → username is `yashzode`

3. **Update the Integration**
   - In `index.html`, update the Cal.com initialization:
   ```javascript
   Cal("init", "your-username", {
       origin: "https://app.cal.com"
   });
   ```
   - Update the inline embed:
   ```javascript
   Cal("inline", {
       elementOrSelector: "#cal-inline",
       calLink: "your-username",
       layout: "month_view"
   });
   ```

4. **Customize Event Types**
   - In your Cal.com dashboard, create event types
   - The booking cards in the portfolio reference:
     - Quick Connect (15 minutes)
     - Consultation (30 minutes)
     - Deep Dive (60 minutes)
   - Update these in the HTML if your event types differ

## 🎨 Customization

### Colors

Edit the CSS variables in `styles.css`:

```css
:root {
    --primary-color: #6366f1;      /* Main brand color */
    --secondary-color: #8b5cf6;     /* Secondary color */
    --accent-color: #ec4899;        /* Accent color */
    /* ... more variables */
}
```

### Content Sections

All content is in `index.html`. Key sections to customize:

- **Hero Section**: Introduction and call-to-action
- **About Section**: Personal background and stats
- **Skills Section**: Technical skills and proficiency
- **Projects Section**: Portfolio projects
- **Services Section**: Services and offerings
- **Booking Section**: Cal.com integration
- **Contact Section**: Contact information and form

### Fonts

The portfolio uses Google Fonts (Inter). To change:

1. Update the font link in `index.html` head
2. Update `font-family` in `styles.css`

## 📱 Responsive Design

The portfolio is fully responsive with breakpoints at:

- **Desktop**: 1200px+
- **Tablet**: 768px - 1199px
- **Mobile**: < 768px
- **Small Mobile**: < 480px

## 🚀 Performance Optimization

- Lazy loading for images
- Optimized CSS and JavaScript
- Minimal external dependencies
- Fast loading times

## 🔒 Security

- All external links use `rel="noopener noreferrer"`
- Form validation included
- No sensitive data stored client-side

## 📝 License

This portfolio template is free to use and modify for personal or commercial projects.

## 🤝 Contributing

Feel free to fork this repository and customize it for your own use. If you make improvements that could benefit others, pull requests are welcome!

## 📧 Support

For questions or issues:
- Open an issue on GitHub
- Contact via the portfolio contact form
- Book a call through Cal.com

## 🎯 Next Steps

1. ✅ Customize all personal information
2. ✅ Update Cal.com username
3. ✅ Add your projects and images
4. ✅ Deploy to GitHub Pages
5. ✅ Share your portfolio!

---

**Built with ❤️ by Yash Zode**

*Last updated: January 2025*

