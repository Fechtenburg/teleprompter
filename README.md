# fechtenburg.github.io
# 🎙 Voice-Driven Teleprompter

A professional teleprompter that listens to your voice and automatically scrolls to keep up with your reading. No internet connection required after the first visit.

Built as a Progressive Web App (PWA) — works directly in Safari on iPhone and iPad, with no App Store required.

-----

## How It Works

The app uses the Web Speech Recognition API built into Safari. As you read your script aloud, the app listens in real time and highlights the current word, automatically scrolling to match your pace.

- **Reading fast?** The scroll speeds up.
- **Pausing?** The scroll stops and waits.
- **Resuming?** It picks up exactly where you left off.

Word matching uses fuzzy similarity (Dice bigram coefficient), so minor mispronunciations or skipped words won’t throw off the position.

-----

## Features

|Feature               |Details                                            |
|----------------------|---------------------------------------------------|
|Voice-driven scrolling|Scroll follows your speech automatically           |
|Word highlighting     |Active word highlighted in amber, past words dimmed|
|Pause detection       |Scroll stops when you stop speaking                |
|Adjustable font size  |24–96px                                            |
|Mirror mode           |For teleprompter glass in front of a camera        |
|Language support      |Danish, English, Norwegian, Swedish, German        |
|Manual position       |Swipe up/down or use « » buttons to jump           |
|Progress bar          |Visual progress across the top of the screen       |
|Offline support       |Service Worker caches everything after first load  |
|PWA                   |Add to home screen for a native app experience     |

-----

## Installation on iPhone / iPad

1. Open the link in **Safari** (not Chrome or Firefox)
1. Tap the **Share** button
1. Tap **Add to Home Screen**
1. The app now works fully offline

> **Note:** Microphone permission is required on first launch. Safari will prompt you automatically.

-----

## Requirements

- Safari on iOS 15 or later
- Microphone access
- HTTPS connection (required for both Speech Recognition and Service Worker)

-----

## Usage

1. Paste your script into the text area
1. Adjust font size and language if needed
1. Tap **START**
1. The microphone activates automatically — start reading
1. Tap the screen to show/hide controls
1. Tap ⏹ to stop listening, 🎙 to resume
1. Tap ✕ to return to the editor

-----

## File Structure

```
index.html      Main app — editor and prompter UI + all JavaScript
manifest.json   PWA manifest for home screen installation
sw.js           Service Worker for offline caching
```

-----

## Privacy

All processing happens locally on your device. No audio, text, or data is ever sent to any server. The speech recognition runs entirely within Safari’s built-in engine.

-----

## Built With

- Vanilla JavaScript — no frameworks, no dependencies
- Web Speech Recognition API (`webkitSpeechRecognition`)
- CSS custom properties and animations
- Service Worker API for offline support

-----

*Built by Thomas Fechtenburg — Technical Bridge-builder*
