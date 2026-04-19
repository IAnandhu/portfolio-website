# Portfolio Website

This is a static HTML portfolio website for Anandu Sivan, Interaction & UX Designer.

## Features

- **Vercel Speed Insights**: Integrated to track and measure web performance metrics
- Responsive design
- Case studies for various projects (Ami, Expo, HelpChat, Radisson)

## Setup

To set up this project locally:

```bash
npm install
npm run build
```

## Build

The build script bundles the Vercel Speed Insights integration:

```bash
npm run build
```

This creates `dist/speed-insights.js` which is loaded by all HTML pages.

## Deployment

This site is configured for deployment on Vercel. The `vercel.json` configuration rewrites the root path to `mockup.html`.

### Vercel Speed Insights

Speed Insights has been configured to automatically track performance metrics when deployed to Vercel. The integration:

1. Loads the Speed Insights script from `/_vercel/speed-insights/script.js` when deployed
2. Automatically captures Core Web Vitals (LCP, FID, CLS, TTFB, INP)
3. Provides performance data in your Vercel dashboard

To enable Speed Insights in your Vercel project:
1. Go to your Vercel dashboard
2. Select your project
3. Navigate to the Speed Insights tab
4. Click "Enable"

## Structure

- `mockup.html` - Main portfolio landing page
- `ami-case-study.html` - Ami case study
- `expo-case-study.html` - Expo case study
- `helpchat-case-study.html` - HelpChat case study
- `radisson-case-study.html` - Radisson case study
- `src/speed-insights.js` - Speed Insights initialization script
- `dist/speed-insights.js` - Bundled Speed Insights script (generated)
