# AI Text Generator - Chrome Built-in Prompting

A modern, elegant web application that leverages Chrome's built-in Language Model API to generate creative text content. This project provides a beautiful, responsive interface for AI-powered text generation directly in your browser.

## ✨ Features

- **Chrome Native Integration**: Uses Chrome's built-in Language Model API for seamless AI text generation
- **Modern UI/UX**: Beautiful gradient design with smooth animations and responsive layout
- **Real-time Status Checking**: Check model availability before generating content
- **Interactive Elements**: Hover effects, loading animations, and smooth transitions
- **Mobile Responsive**: Optimized for all device sizes
- **Keyboard Support**: Press Enter to generate text from the input field

## 🚀 Getting Started

### Prerequisites

- **Google Chrome Browser**: Version 114+ with Chrome's Language Model API enabled
- **Chrome Flags**: Enable the experimental Language Model API

### Setup Instructions

1. **Enable Chrome Flags**:
   - Open Chrome and navigate to `chrome://flags/`
   - Search for "Language Model API" or "Chrome AI"
   - Enable the relevant flags for Language Model support
   - Restart Chrome

2. **Run the Application**:
   ```bash
   # Simply open the index.html file in Chrome
   open index.html
   ```
   
   Or serve it locally:
   ```bash
   # Using Python
   python -m http.server 8000
   
   # Using Node.js
   npx serve .
   
   # Using PHP
   php -S localhost:8000
   ```

3. **Access the Application**:
   - Navigate to `http://localhost:8000` (if using a local server)
   - Or open `index.html` directly in Chrome

## 📖 Usage

### Basic Text Generation

1. **Enter a Prompt**: Type your desired text prompt in the input field
2. **Generate Text**: Click the "✨ Generate Text" button or press Enter
3. **View Results**: The generated text will appear in the output section

### Check Model Availability

1. **Check Status**: Click the "🔍 Check Availability" button
2. **View Status**: The current model status will be displayed:
   - ✅ **Available**: Model is ready to use
   - ❌ **Unavailable**: Model is not available
   - ⏳ **Downloadable**: Model can be downloaded
   - 📥 **Downloading**: Model is currently downloading

## 🎨 Features in Detail

### User Interface
- **Gradient Background**: Beautiful purple-blue gradient background
- **Glass Morphism**: Semi-transparent container with backdrop blur
- **Smooth Animations**: Fade-in effects and hover transitions
- **Loading States**: Animated spinner during text generation
- **Status Indicators**: Clear visual feedback for all operations

### Technical Features
- **Async/Await**: Modern JavaScript for smooth user experience
- **Error Handling**: Graceful error handling with user-friendly messages
- **Event Listeners**: Keyboard support and button interactions
- **Dynamic Styling**: Real-time UI updates based on application state

## 🔧 Technical Implementation

### Chrome Language Model API
The application uses Chrome's built-in `LanguageModel` API:

```javascript
// Check model availability
const availability = await LanguageModel.availability();

// Create a session and generate text
const session = await LanguageModel.create();
const result = await session.prompt(prompt);
```

### CSS Features
- **CSS Grid & Flexbox**: Modern layout techniques
- **CSS Variables**: Consistent theming
- **Media Queries**: Responsive design
- **CSS Animations**: Smooth transitions and effects

## 📱 Browser Compatibility

- **Primary**: Google Chrome 114+ with Language Model API enabled
- **Fallback**: Other browsers will show the interface but may not support AI generation

## 🛠️ Development

### Project Structure
```
chrome-ai/
├── index.html          # Main application file
├── README.md          # This documentation
└── .gitignore         # Git ignore file (if using version control)
```

### Customization
- **Colors**: Modify the CSS gradient values in the `:root` section
- **Styling**: Update the CSS classes for different visual themes
- **Functionality**: Extend the JavaScript functions for additional features

## 🚨 Troubleshooting

### Common Issues

1. **"LanguageModel is not defined"**
   - Ensure Chrome flags are enabled
   - Restart Chrome after enabling flags
   - Check Chrome version compatibility

2. **Model not available**
   - Wait for model download to complete
   - Check internet connection
   - Try refreshing the page

3. **Generation fails**
   - Check browser console for errors
   - Ensure prompt is not empty
   - Verify Chrome Language Model API is working

### Debug Mode
Open Chrome DevTools (F12) to view console logs and debug information.
---

**Note**: This application requires Chrome's experimental Language Model API. The API is subject to change and may not be available in all Chrome versions or configurations. 
