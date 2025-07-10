# VectorStrat Advisory Website

A clean, elegant website for VectorStrat Advisory - Investment Management Consulting.

## Features

- **Clean, Professional Design**: Minimalist and elegant styling
- **Responsive Layout**: Works perfectly on desktop, tablet, and mobile
- **Contact Form**: Integrated contact form with validation
- **Smooth Navigation**: Smooth scrolling between sections
- **Professional Typography**: Using Inter font for modern readability

## File Structure

```
VectorStrat/
├── index.html          # Main website file
├── styles.css          # All styling
├── script.js           # JavaScript functionality
├── BL Headshot.jpeg    # Profile image
└── README.md           # This file
```

## Setup

1. **Local Development**: Simply open `index.html` in your web browser
2. **Web Hosting**: Upload all files to your web hosting provider

## Email Integration

The contact form currently shows a success message but doesn't actually send emails. To enable real email functionality, choose one of these options:

### Option 1: EmailJS (Recommended - No Backend Required)

1. Sign up at [EmailJS](https://www.emailjs.com/)
2. Create an email template
3. Replace the form submission code in `script.js` with EmailJS integration:

```javascript
// Add EmailJS SDK to HTML head
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@3/dist/email.min.js"></script>

// Initialize EmailJS
emailjs.init("YOUR_USER_ID");

// Replace the setTimeout in script.js with:
emailjs.send("YOUR_SERVICE_ID", "YOUR_TEMPLATE_ID", {
    name: data.name,
    email: data.email,
    company: data.company,
    service: data.service,
    message: data.message
}).then(
    function(response) {
        alert('Thank you for your message! I will get back to you soon.');
        form.reset();
    },
    function(error) {
        alert('Sorry, there was an error. Please try again.');
    }
);
```

### Option 2: Formspree

1. Sign up at [Formspree](https://formspree.io/)
2. Add the form action to your HTML form:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 3: Netlify Forms

1. Deploy to Netlify
2. Add `netlify` attribute to your form:
```html
<form netlify>
```

## Customization

### Colors
The website uses a clean black and white color scheme. To change colors, modify the CSS variables in `styles.css`.

### Content
- Update the hero section text in `index.html`
- Modify services in the services section
- Update the about section with your specific background
- Replace the headshot image with your own

### Contact Form
- Add/remove form fields as needed
- Customize validation rules in `script.js`
- Update success/error messages

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance

- Optimized images
- Minimal JavaScript
- Fast loading times
- Mobile-optimized

## License

This project is for VectorStrat Advisory use only. 