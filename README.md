# Teleprompter PWA

A professional, voice-controlled teleprompter app built as a Progressive Web App (PWA), specifically designed for iOS (Safari) but fully functional on other modern browsers. This app listens while you read and automatically scrolls the text, so you never lose your place.

## 🚀 Features

- **Voice-Controlled Scrolling:** The app uses the Web Speech API to listen to your voice. It highlights the active word as you read and accurately scrolls the text as you progress, pausing exactly when you do.
- **Mirror Mode:** Can mirror the text, making it perfect for use in physical teleprompter rigs with a beam-splitter glass.
- **Multi-Language Support:** Supports speech recognition for multiple languages: Danish (DA), English (EN), Norwegian (NO), Swedish (SV), and German (DE).
- **Text Customization:** Easily adjust the text size directly within the app to fit your reading distance.
- **Touch & Swipe Controls:** You can easily swipe up or down to manually jump forward or backward in the text while presenting.
- **Offline Support:** Because the app is a PWA with a Service Worker (`sw.js`), it can be installed on your device's home screen (Add to Home Screen) and used completely offline after the very first load.
- **Focus Mode:** Clean, dark overlay in prompter mode with a subtle focus line, making it very easy on the eyes.

## 🛠 Technical Overview

The app is built using clean, modern web technologies and is completely independent of heavy frameworks:
- **HTML/CSS/JavaScript (Vanilla):** Everything is written in a single primary HTML document for simple distribution and lightning-fast loading times.
- **Web Speech API:** Handles the voice recognition by continuously listening to the microphone via Interim Results. 
- **Dice Bigram Similarity:** An advanced, built-in "fuzzy matching" algorithm that compares spoken words with the script, preventing the app from jumping unpredictably if a word is mispronounced or incorrectly recognized (especially on iOS Safari).

## 📂 Project Files

- `index.html`: The application itself. Contains the entire UI (Editor and Prompter), CSS styling, and JavaScript logic.
- `manifest.json`: Web app manifest that allows the app to be installed (PWA) and defines colors, icons, and display mode (fullscreen).
- `sw.js`: The Service Worker file that handles caching. It uses a Network-First strategy to ensure you always get the latest updates when online, but smoothly falls back to offline caching when disconnected.

## 💡 How to Use

1. Open `index.html` in a modern browser (Safari on iOS 15+ is recommended for optimal speech recognition).
2. Paste your script into the text area on the start screen.
3. Adjust text size, language, and mirror mode as needed.
4. Press **START ▶**.
5. The app will ask for microphone access the first time. Allow it.
6. Start reading aloud. The app will automatically highlight the words and scroll at your pace!

---
*Developed with a focus on reliability and user-friendliness during video recordings.*
