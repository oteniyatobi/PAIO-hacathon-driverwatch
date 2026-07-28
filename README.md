# DriverWatch Enterprise

DriverWatch Enterprise is a web-based driver safety platform that combines live camera monitoring, AI fatigue detection, alert escalation, incident recording, and cloud-connected evidence management. The project is designed for real-time monitoring and can be packaged for Android with Capacitor.

## What the app does

- Streams a live camera feed and shows system status, camera health, and telemetry
- Uses a TensorFlow.js / Teachable Machine model to classify the driver as awake or drowsy
- Escalates from a warning state to audible alerts and emergency handling when fatigue persists
- Records driving sessions and generates downloadable incident clips in WebM format
- Tracks speed, location, and event history for safety monitoring
- Supports Firebase and Supabase-backed recording workflows and alert integrations

## Core features

- Real-time fatigue detection with alert logic
- Warning beeps and siren escalation for unsafe driver states
- Instant incident clip creation and download
- Continuous session recording with REC indicators
- Speed monitoring and speeding alerts
- Location tracking and event logging
- User profile support and recording history
- Capacitor-based Android build support

## Tech stack

- Frontend: HTML, CSS, JavaScript
- AI inference: TensorFlow.js and Teachable Machine model
- Media handling: MediaRecorder and Web Audio API
- Backend services: Firebase Firestore / Firebase Admin, Supabase, Twilio
- Mobile packaging: Capacitor for Android

## Project structure

- app.js and www/app.js: main application logic
- index.html and www/index.html: user interface
- scripts/build-web.js: web build step
- api/: server-side endpoints for recording and alert workflows
- android/: Capacitor Android project

## Run locally

1. Install dependencies
   ```bash
   npm install
   ```
2. Start the local web server
   ```bash
   npm start
   ```
3. Open http://localhost:3000 in a browser
4. Allow camera access and click Start Monitoring

## Build for Android

```bash
npm run cap:sync
npm run cap:open
```

## Notes

- Camera access requires a local server or HTTPS and browser permission
- Some cloud-connected features depend on configured Firebase, Supabase, or Twilio credentials

