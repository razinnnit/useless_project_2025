# OLDVIS - Voice Interface System

A futuristic AI voice interface that combines the aesthetics of Iron Man's JARVIS with the functionality of Interstellar's TARS, powered by humorous mishearing logic.

## 🎯 Features

### 🎤 **Real Voice Recognition**
- **Web Speech API Integration**: Real-time speech-to-text using browser's built-in speech recognition
- **Continuous Listening**: Seamless voice input with automatic processing
- **Error Handling**: Graceful fallbacks for unsupported browsers or recognition errors

### 🤖 **Mishearing AI Logic**
- **Contextual Responses**: AI responds to specific keywords with humorous misunderstandings
- **Category Detection**: Recognizes commands for music, alarms, apps, camera, calls, files, weather, lights, and search
- **Random Humor**: Fallback responses that are completely absurd and entertaining
- **Audio Integration**: Optional audio responses alongside text (when audio files are available)

### 🎨 **Futuristic UI**
- **Glass Morphism Design**: Modern, translucent interface with backdrop blur effects
- **Real-time Chat**: Live conversation display with message history and timestamps
- **Interactive Elements**: Hover effects, animations, and visual feedback
- **Responsive Layout**: Works on desktop, tablet, and mobile devices

### 🔧 **Technical Features**
- **TypeScript**: Full type safety and better development experience
- **Next.js 14**: Modern React framework with App Router
- **Tailwind CSS**: Utility-first styling with custom animations
- **Custom Hooks**: Reusable speech recognition and processing logic

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- npm or pnpm
- Modern browser with Web Speech API support (Chrome, Edge, Safari)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd jarvis-main
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   pnpm install
   ```

3. **Start the development server**
   ```bash
   npm run dev
   # or
   pnpm dev
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

## 🎮 How to Use

### Voice Commands
OLDVIS responds to various voice commands with humorous misunderstandings:

- **Music**: "play music", "spotify", "song", "playlist"
- **Alarms**: "set alarm", "timer", "wake up", "reminder"
- **Apps**: "open chrome", "launch app", "start youtube"
- **Camera**: "take photo", "selfie", "camera"
- **Calls**: "call someone", "text message", "phone"
- **Files**: "delete files", "organize", "downloads"
- **Weather**: "check weather", "forecast", "temperature"
- **Lights**: "turn on lights", "bright", "dark"
- **Search**: "search google", "find", "look up"

### Interface Controls
- **SPEAK Button**: Click to start/stop voice recognition
- **Live Chat**: View conversation history in real-time
- **Status Indicators**: Visual feedback for system status

## 🏗️ Project Structure

```
jarvis-main/
├── app/
│   ├── page.tsx              # Main OLDVIS interface
│   ├── layout.tsx            # Root layout
│   └── globals.css           # Global styles
├── lib/
│   └── logic/
│       └── mishearing.ts     # AI response logic
├── hooks/
│   └── useSpeechRecognition.ts # Speech recognition hooks
├── types/
│   └── speech.d.ts           # TypeScript declarations
├── public/
│   └── audio/                # Audio response files
└── components/               # Reusable UI components
```

## 🎨 Customization

### Adding New Response Categories
Edit `lib/logic/mishearing.ts` to add new categories:

```typescript
const responses = {
  newcategory: [
    { text: "Your humorous response here", audio: "/audio/audio1.mp3" },
    { text: "Another funny response", audio: null }
  ]
};

const categories = [
  { key: "newcategory", keywords: ["keyword1", "keyword2"] }
];
```

### Styling Customization
- Modify `app/globals.css` for custom animations
- Update `tailwind.config.ts` for theme changes
- Edit `app/page.tsx` for layout modifications

### Audio Integration
Add audio files to `public/audio/` directory:
- audio1.mp3 through audio9.mp3
- System will gracefully handle missing files

## 🔧 Technical Details

### Speech Recognition
- Uses Web Speech API (`webkitSpeechRecognition`)
- Continuous listening with interim results
- Automatic language detection (en-US)
- Error handling for unsupported browsers

### State Management
- React hooks for local state
- Custom hooks for speech processing
- Real-time message updates
- Audio playback management

### Performance
- Optimized builds with Next.js
- Lazy loading and code splitting
- Efficient re-renders with React hooks
- Smooth 60fps animations

## 🌟 Features in Detail

### Mishearing Logic
The AI intentionally misunderstands user commands to create humorous responses:

1. **Keyword Detection**: Scans user input for specific keywords
2. **Category Matching**: Maps keywords to response categories
3. **Random Selection**: Picks random response from matching category
4. **Fallback Logic**: Uses random responses for unrecognized commands

### Voice Processing Pipeline
1. **Speech Input**: User speaks into microphone
2. **Recognition**: Web Speech API converts speech to text
3. **Processing**: Mishearing logic generates response
4. **Output**: Text response + optional audio playback
5. **Display**: Updates UI with conversation history

## 🐛 Troubleshooting

### Speech Recognition Issues
- **Not Working**: Ensure you're using a supported browser (Chrome, Edge, Safari)
- **Permission Denied**: Allow microphone access when prompted
- **No Response**: Check browser console for error messages

### Build Issues
- **TypeScript Errors**: Run `npm run build` to check for type issues
- **Missing Dependencies**: Run `npm install` to install missing packages
- **Port Conflicts**: Change port in `package.json` if 3000 is in use

### Audio Issues
- **No Audio**: Audio files are optional - system works without them
- **Audio Not Playing**: Check browser autoplay policies
- **File Not Found**: Ensure audio files are in `public/audio/` directory

## 🚀 Deployment

### Vercel (Recommended)
1. Push code to GitHub
2. Connect repository to Vercel
3. Deploy automatically

### Other Platforms
- **Netlify**: Use `npm run build` and deploy `out/` directory
- **Railway**: Connect GitHub repository
- **Docker**: Use provided Dockerfile

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Web Speech API**: For voice recognition capabilities
- **Next.js Team**: For the amazing React framework
- **Tailwind CSS**: For the utility-first styling approach
- **Iron Man & Interstellar**: For design inspiration

---

**OLDVIS** - Where AI meets humor, one misheard command at a time! 🎭
