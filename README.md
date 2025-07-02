# Surgicure ROI Frontend

This project is a simple, interactive front-end application for Surgicure’s ROI Calculator. It allows hospital stakeholders to enter key data—or use national averages—to generate a real-time cost savings estimate for endotracheal tube (ETT) intervention in ICU settings.

Built with Next.js and deployable via Vercel.

## Features

- Input-driven ROI estimator
- Supports both default and custom assumptions
- Calls GPT model via secure API route
- Fully client-rendered interface
- Clean, minimal design with responsive layout

## Technology Stack

- Next.js (React Framework)
- TypeScript
- OpenAI API (via /api/roi route)
- Deployment-ready for Vercel

## Getting Started

1. Clone the repo

   git clone https://github.com/YOUR_USERNAME/surgicure-roi-frontend.git
   cd surgicure-roi-frontend

2. Install dependencies

   npm install

3. Create your .env.local file

   OPENAI_API_KEY=sk-...

   You must obtain an OpenAI API key to use the GPT-powered backend.

4. Run the development server

   npm run dev

   Then open your browser to http://localhost:3000

## Deploy to Vercel

1. Go to https://vercel.com/import
2. Select your GitHub repository
3. Add the OPENAI_API_KEY as an environment variable
4. Click "Deploy"

## How It Works

The interface collects hospital size, toggles for default values, and clinical efficacy settings. When submitted, the form calls /api/roi, which sends a structured prompt to OpenAI’s GPT-4 model.

The GPT returns a natural-language ROI breakdown, which is rendered to the screen.

## Project Structure

components/
  ROIForm.tsx        → User input form
pages/
  index.tsx          → Main page
  api/roi.ts         → API route calling OpenAI

## License

MIT — free for use with Surgicure attribution or modification.

## Need Help?

Contact your Surgicure development team or open an issue in the repo.
