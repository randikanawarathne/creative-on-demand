# Creative on Demand

A powerful brand asset generator that allows you to create stunning social media posts using predefined master templates. Input your text, upload an image, and instantly generate professionally designed social media content with consistent branding.

## 🎨 Features

- **3 Professional Templates**
  - **Bold Impact**: Full-bleed image with dramatic overlay and vertical accent bar
  - **Modern Split**: Image alongside bold colored section with geometric accents
  - **Elegant Frame**: Centered image with refined border and editorial layout

- **Real-Time Preview**: See your changes instantly as you type and upload images
- **Drag & Drop Image Upload**: Easy image upload with preview
- **Live Text Editing**: Headline and tagline with automatic font scaling
- **One-Click Download**: Export your designs as high-resolution PNG files
- **Fully Responsive**: Works seamlessly on desktop, tablet, and mobile devices
- **Dark Theme**: Modern, sleek interface with accent colors for better focus

## 🚀 Quick Start

### No Installation Required!
Simply open `index.html` in your web browser. The entire application runs client-side with no external dependencies (except Google Fonts for typography).

### How to Use

1. **Select a Template**: Choose from the 3 available templates at the top
2. **Enter Your Text**: 
   - Add a headline (max 50 characters)
   - Add a tagline (optional, max 100 characters)
   - Enter your brand name for the watermark
3. **Upload an Image**: Drag and drop or click to browse
4. **Download**: Click the download button to save your design as PNG

## 🛠️ Technical Stack

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS custom properties and Flexbox
- **JavaScript (Vanilla)**: Pure JS with HTML5 Canvas API
- **Google Fonts**: Bebas Neue, DM Sans, Playfair Display, Oswald, Montserrat

**No Dependencies**: Zero external libraries - all functionality is built from scratch using web standards.

## 📐 Design Specifications

### Templates
- **Templates 1 & 2**: 1080x1080px (Instagram Square Format)
- **Template 3**: 1080x1350px (Portrait/Story Format)

### Input Constraints
- **Headline**: Max 50 characters (required)
- **Tagline**: Max 100 characters (optional)
- **Image**: JPG/PNG, minimum 400x400px
- **Brand Name**: Max 30 characters

### Color Palette
- **Primary**: `#0d0d14` (Deep dark navy)
- **Accent**: `#e94560` (Coral red)
- **Template 1**: `#00d9ff` (Cyan)
- **Template 2**: `#ff6b35` (Orange)
- **Template 3**: `#7b2cbf` (Purple)

## 📱 Browser Support

- Chrome/Chromium (Latest)
- Firefox (Latest)
- Safari (Latest)
- Edge (Latest)

## 🎯 Use Cases

Perfect for:
- **Marketing Teams**: Create consistent branded social media posts
- **Small Business Owners**: Generate professional content without design skills
- **Consultants**: Quick branded assets for client communication
- **Content Creators**: Fast, templated design process for high-volume posting

## 📝 File Structure

```
index.html          # Main application file (HTML + CSS + JS)
SPEC.md             # Detailed project specification
README.md           # This file
```

## ⚙️ Performance Features

- **Debounced Rendering**: 150ms debounce for smooth performance
- **High-Resolution Output**: 2x rendering for Retina display compatibility
- **Optimized Canvas Rendering**: Efficient real-time preview updates
- **Auto Font Scaling**: Text automatically scales to fit without overflow (minimum 24px)

## 🎓 How It Works

1. **Canvas Rendering**: The application uses HTML5 Canvas API to draw templates with user input
2. **Real-Time Updates**: Debounced JavaScript updates the preview as you modify inputs
3. **Image Handling**: Uploaded images are processed with proper scaling and positioning
4. **PNG Export**: Final design is rendered at full resolution and downloaded as PNG

## 📄 License

This project is open source and available for personal and commercial use.

## 🤝 Contributing

Contributions are welcome! Feel free to fork this repository and submit pull requests for improvements.

## 📮 Support

For issues, feature requests, or questions, please open an issue on GitHub.

---

**Created**: 2026 | **Last Updated**: March 4, 2026
