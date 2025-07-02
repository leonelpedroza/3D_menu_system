# 3D Interactive Menu System

A stunning dual-menu system featuring a 3D spherical social media carousel and an interactive rotating cube menu, built with pure HTML, CSS, and JavaScript.

![3D Menu Preview](https://img.shields.io/badge/Preview-Live_Demo-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 🌟 Features

### Spherical Social Media Carousel
- **11 Social Media Platforms**: LinkedIn, GitHub, Discord, Facebook, X/Twitter, Instagram, YouTube, TikTok, Pinterest, Quora, and Reddit
- **3D Spherical Distribution**: Icons arranged in a perfect sphere using mathematical calculations
- **Interactive Rotation**: Mouse-controlled rotation with realistic physics
- **Inertia System**: Smooth momentum-based movement that continues after mouse release
- **Auto-rotation**: Gentle continuous rotation when idle
- **Hover Effects**: Icons transition from grayscale to full color with brand-specific backgrounds
- **Smart Tooltips**: Platform names appear on hover
- **Auto-close Timer**: Sphere automatically closes after 30 seconds of inactivity

### Cube Menu
- **6 Customizable Faces**: Each face can display different images and link to different URLs
- **Hover Expansion**: Cube grows from 30px to 100px on hover
- **Auto-rotation**: Continuous rotation when not interacted with
- **Mouse-controlled Rotation**: Direct manipulation with smooth physics
- **Inertia Effects**: Realistic momentum when mouse is released

## 🚀 Demo

```html
<!-- Simply open menu.html in a modern web browser -->
```
<p align="center">
    <img src="https://github.com/leonelpedroza/3D_menu_system/screenshot1.png">
    <img src="https://github.com/leonelpedroza/3D_menu_system/screenshot2.png">
</p>




## 📋 Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Opera

*Note: Requires browsers with CSS 3D transforms support*

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/leonelpedroza/3d-interactive-menu.git
```

2. Navigate to the project directory:
```bash
cd 3d-interactive-menu
```

3. Open `menu.html` in your web browser

## 📁 Project Structure

```
3d-interactive-menu/
│
├── menu.html           # Main HTML file with all code
├── Picture/           # Directory for cube face images
│   ├── Picture1.png   # Front face image
│   ├── picture2.png   # Back face image
│   ├── picture3.png   # Right face image
│   ├── picture4.png   # Left face image
│   ├── picture5.png   # Top face image
│   └── picture6.png   # Bottom face image
└── README.md          # This file
```

## 🎨 Customization

### Changing Social Media Links

Find the social media links in the HTML and update the `href` attributes:

```html
<a href="https://www.linkedin.com/" target="_blank" class="social-icon linkedin" data-name="LinkedIn">
    <!-- SVG icon -->
</a>
```

### Customizing Cube Menu

1. **Change Images**: Replace the images in the `Picture/` folder
2. **Update Links**: Modify the `href` attributes in the cube faces:

```html
<div class="cube-face face-front" style="background-image: url('Picture/Picture1.png');">
    <a href="https://www.google.com/" target="_blank" title="Picture 1"></a>
</div>
```

### Adjusting Animation Speed

- **Sphere Auto-rotation**: Modify the velocity values in `startSlowRotation()`
- **Cube Auto-rotation**: Change the animation duration in CSS:
```css
animation: rotateCube 10s infinite linear; /* Change 10s to desired duration */
```

### Changing Colors

- **Sphere Trigger Button**: Update the gradient in `.sphere-trigger`
- **Social Media Colors**: Modify the hover colors for each platform in CSS

## 🔧 Technical Details

### Sphere Mathematics

The sphere uses spherical coordinates to evenly distribute icons:

```javascript
const phi = Math.acos(-1 + (2 * index) / numIcons);
const theta = Math.sqrt(numIcons * Math.PI) * phi;
```

### Physics Implementation

- **Velocity Calculation**: Based on mouse movement delta
- **Friction**: 0.98 multiplier for smooth deceleration
- **Inertia Duration**: ~5+ seconds of continued movement

### Performance Optimizations

- Uses `transform3d` for hardware acceleration
- `requestAnimationFrame` for smooth animations
- Event delegation for efficient event handling

## 📝 Code Structure

The code is organized into three main sections:

1. **HTML Structure**: Semantic markup for both menu systems
2. **CSS Styling**: Comprehensive styles with 3D transforms
3. **JavaScript Logic**: Separated concerns for sphere and cube functionality

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👏 Acknowledgments

- Social media icons use official brand colors
- Inspired by modern 3D web interactions
- Built with vanilla JavaScript for maximum compatibility

## 📧 Contact

Your Name - [@leonelpedroza](https://x.com/leonelpedroza) - leonelpedroza@gmail.com

Project Link: [https://github.com/leonelpedroza/3d-interactive-menu](https://github.com/leonelpedroza/3d-interactive-menu)

---

⭐ If you find this project useful, please consider giving it a star!
