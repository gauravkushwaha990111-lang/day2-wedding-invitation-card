# 💒 Premium 3D Web Wedding Invitation

A highly interactive, cinematic, and luxurious web-based wedding invitation for **Aarav & Anu**. Built with modern web technologies to deliver a "Wow" experience, featuring a 3D gatefold envelope, interactive particles, smooth scroll animations, and a dynamic 3D photo gallery.

## ✨ Key Features

- **Royal 3D Gatefold Entrance:** A beautiful envelope opening animation with wax seal pop and page-flip sound effect.
- **Cinematic Background & Music:** Soothing romantic background music (with autoplay workaround) and an interactive 3D particle background (Three.js) that reacts to mouse movement (Repel/Blast effect).
- **Force Landscape Mode:** Ensures mobile users get the best cinematic experience by prompting them to rotate their phones.
- **Interactive Elements:**
  - Floating magical hearts on click.
  - Custom glowing cursor (for desktop).
  - Confetti blasts on RSVP and "Save the Date" actions.
  - Scroll progress bar.
- **Live Countdown:** Real-time countdown timer to the wedding date.
- **Animated "Our Story" Timeline:** Beautiful GSAP scroll-triggered animations showcasing the couple's journey.
- **Event Management:** Detailed itinerary with instant "View on Google Maps" and "Copy Address" buttons.
- **3D Interactive Gallery:** A rotating 3D carousel for memories, complete with a fullscreen Lightbox modal.
- **Virtual Shagun & RSVP:** 
  - Form UI for guests to RSVP.
  - Auto-generating UPI QR code for virtual blessings (Shagun).
- **Easy Configuration:** A central `config.js` file to easily update names, dates, locations, UPI, and images without touching the HTML.

## 🚀 Technologies Used

- **HTML5 & CSS3** (Tailwind CSS via CDN for rapid, responsive styling)
- **JavaScript (ES6+)**
- **Three.js:** For the high-performance 3D glowing particle environment.
- **GSAP (GreenSock) & ScrollTrigger:** For buttery smooth scroll animations and reveals.
- **Canvas Confetti:** For celebration particle effects.
- **FontAwesome:** For elegant UI icons.
- **Google Fonts:** Playfair Display (Serif) & Plus Jakarta Sans (Sans-serif).

## 📂 Project Structure

```text
wedding/
├── index.html       # The main invitation template and UI
├── config.js        # Central configuration file for easy content updates
└── README.md        # Project documentation
```

## ⚙️ Setup & Installation

Because this project uses ES Modules (`type="module"`) for Three.js and GSAP, opening `index.html` directly by double-clicking might cause CORS (Cross-Origin Resource Sharing) errors in some browsers. 

**To run it properly:**

1. Use a local web server. If you use VS Code, install the **Live Server** extension.
2. Right-click on `index.html` and select **"Open with Live Server"**.
3. The invitation will seamlessly load in your default browser.

## 🛠️ Customization (How to update details)

You don't need to dig into the complex HTML/JS to update the wedding details! Simply open `config.js` and modify the values:

```javascript
const config = {
    weddingDate: '2025-12-15T19:00:00', // Update your countdown target
    coupleName: 'Aarav & Anu',          // Update couple names

    mainEvent: {
        address: 'Your Address Here',
        mapQuery: 'Google Maps Search Query'
    },
    
    upi: {
        id: 'yourname@upi',
        name: 'Your Name',
        qrImage: '' // Leave empty to auto-generate, or paste a link to your custom QR
    },

    galleryImages: [
        'link-to-image-1.jpg',
        'link-to-image-2.jpg'
    ]
};
```