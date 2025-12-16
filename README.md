Open source Earth zoom animation recording tool by Wplace.ai. Create stunning videos showcasing locations, travel routes, and geographic stories with smooth zoom animations from space to street level.

🔗 Part of the Wplace.ai ecosystem - A platform for discovering and sharing location-based content with yuteng.online insights.

✨ Features
Multiple Recording Modes

Canvas recording for pure map content (higher quality)
Screen capture for complete interface recording with audio support
World Tour Presets

Pre-built animation sequences featuring world capitals
Natural wonders and famous landmarks
Customizable animation paths
High-Quality Recording

Support for up to 4K resolution
60fps frame rates
Efficient WebM compression
Instant browser-based export
Professional Tools

Smooth animation engine with cinematic easing
Configurable recording settings
Real-time preview and controls
No server uploads required
🚀 Quick Start
Prerequisites
Node.js 18+ and npm
A Mapbox access token (free at mapbox.com)
Installation
Clone and install dependencies

git clone <repository-url>
cd mapbox-earth-recorder
npm install
Set up your Mapbox token

Get a free token from Mapbox
Copy .env.example to .env.local
Add your token to the .env.local file:
NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN=pk.your-actual-token-here
Start the development server

npm run dev
Open your browser

Visit http://localhost:3000
Click "Launch Studio" to start recording
🎬 How to Use
Manual Recording
Open the Earth Zoom Recorder panel
Choose "Manual" mode
Configure your recording settings (quality, duration, etc.)
Click "Start Recording"
Navigate the Earth by zooming and panning
Click "Stop Recording" when done
Download your video instantly
World Tour Recording
Select "Tour" mode
Choose from built-in presets:
Classic World Tour (8 major cities)
Natural Wonders (8 amazing locations)
Asian Capitals (9 cities)
Mediterranean Coast (10 coastal cities)
And more!
Click "Start Tour" to begin automatic recording
The camera will smoothly transition between locations
Download your completed tour video
🛠️ Recording Settings
Canvas Mode: Records only the map (recommended for highest quality)
Screen Mode: Records your entire screen (captures popups and overlays)
Quality Options: Low (1Mbps), Medium (2.5Mbps), High (5Mbps)
Frame Rates: 24fps, 30fps, 60fps
Duration: 5s, 10s, 15s, or manual stop
🏗️ Project Structure
mapbox-earth-recorder/
├── app/                    # Next.js 15 App Router
│   ├── page.tsx           # Landing page
│   └── studio/page.tsx    # Recording studio
├── components/
│   ├── map-studio.tsx     # Main map component
│   ├── earth-zoom-recorder.tsx  # Recording controls
│   └── ui/                # Reusable UI components
├── lib/
│   ├── video-recorder.ts  # Core recording engine
│   ├── animation/         # Animation system
│   └── presets.ts        # Built-in tour presets
└── public/               # Static assets
🎯 Built-in Animation Presets
World Tours
Classic World Tour: New York → London → Paris → Tokyo → Dubai → Sydney → São Paulo → Cairo
Asian Capitals: Beijing → Seoul → Tokyo → Bangkok → Singapore → KL → Jakarta → Manila → Delhi
Mediterranean Coast: Barcelona → Nice → Rome → Dubrovnik → Athens → Istanbul → Santorini → Cyprus
Natural Wonders
Natural Wonders: Grand Canyon → Everest → Great Barrier Reef → Amazon → Sahara → Victoria Falls
Modern Skylines: Manhattan → Dubai → Hong Kong → Singapore → Shanghai → London
Special Effects
Space to Earth: Global view → Continent → Country → City → Street level
Custom Paths: Create your own animation sequences
🔧 Advanced Usage
Custom Animation Presets
You can create custom animation presets by modifying lib/presets.ts:

const myCustomPreset: AnimationPreset = {
  id: 'my-tour',
  name: 'My Custom Tour',
  description: 'A personalized journey',
  duration: 30,
  category: 'custom',
  difficulty: 'easy',
  stops: [
    { name: 'Start', coordinates: [lng, lat], zoom: 10, duration: 3 },
    { name: 'End', coordinates: [lng2, lat2], zoom: 12, duration: 3 }
  ]
};
Recording Configuration
Adjust recording parameters in the component:

const recordingOptions: RecordingOptions = {
  mode: 'canvas',              // or 'screen'
  videoBitsPerSecond: 5000000, // 5 Mbps for high quality
  frameRate: 60,               // Smooth 60fps
  mimeType: 'video/webm;codecs=vp9'
};
🌐 Browser Support
✅ Chrome 88+ (recommended)
✅ Firefox 85+
✅ Safari 14+
✅ Edge 88+
Note: Canvas recording requires captureStream() support. Screen recording requires getDisplayMedia() API.

🚀 Deployment
Vercel (Recommended)
Push your code to GitHub
Connect your repo to Vercel
Add your NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN environment variable
Deploy!
Other Platforms
Netlify: Works with static export
Railway: Full Next.js support
Self-hosted: Use npm run build && npm run start
📝 Development
Commands
npm run dev - Start development server
npm run build - Build for production
npm run start - Start production server
npm run lint - Run ESLint
Key Technologies
Next.js 15 - App Router with React 18
Mapbox GL JS - Interactive map rendering
TypeScript - Type-safe development
Tailwind CSS - Utility-first styling
MediaRecorder API - Native browser recording
Canvas API - High-performance graphics
🤝 Contributing
Fork the repository
Create a feature branch: git checkout -b feature/amazing-feature
Commit changes: git commit -m 'Add amazing feature'
Push to branch: git push origin feature/amazing-feature
Open a Pull Request
📄 License
MIT License - see the LICENSE file for details.

🌎 About yuteng.online
This Earth Zoom Recorder is part of the Wplace.ai platform ecosystem. yuteng.online offers:

🗺️ Location Discovery: Search any location and get AI-curated information about food, hotels, attractions, and local history
📍 Interactive Pins: Pin your own media content to locations and discover what others have shared around the world
🎬 Video Recording: Create stunning Earth zoom videos to showcase your favorite locations and travel stories
🤖 AI Integration: Get intelligent summaries and recommendations for any location using advanced AI technology
Visit Wplace.ai to explore the full platform and discover amazing places around the world!

🙏 Acknowledgments
Wplace.ai for sponsoring this open source project
Mapbox for the amazing mapping platform
Next.js team for the fantastic framework
shadcn/ui for the beautiful components
Lucide for the clean icons
📧 Support
GitHub Issues: Bug reports and feature requests
Wplace.ai Community: Visit Wplace.ai for community discussions
Documentation: Check this README for detailed guides
Open Source by Wplace.ai • Powered by Mapbox GL JS
