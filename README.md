# Contract Risk Analyzer

Welcome to the **Contract Risk Analyzer** project.

Contract Risk Analyzer is a web application that lets users sign up, upload contract PDFs, and get an automatic risk analysis (High / Medium / Low).  
The app also highlights positive elements in the contract, provides export options for the analysis, and maintains a history of the user’s previously analyzed contracts.

> Note: This project was initially scaffolded using a template and then customized with Supabase, Tailwind CSS, and TypeScript.

---

## Quick Start

1. **Install dependencies**

   ```bash
   npm install
   ```

2. **Install Tailwind CSS (if not already installed)**

   ```bash
   npm install -D tailwindcss
   ```

3. **Run the project**

   ```bash
   npm run dev
   ```

---

## Features

- **User authentication**  
  - Sign up / log in functionality using Supabase Auth.  
  - Each user sees only their own analysis history.

- **Contract PDF upload**  
  - Users can upload contract PDF files from the browser.  
  - The contract content is sent for analysis and processed on the backend.

- **Risk analysis**  
  - Each contract is classified into a **risk level**: High, Medium, or Low.  
  - The UI uses color coding for quick visual understanding.

- **Positive clause suggestions**  
  - The app surfaces **good / safe parts** of the contract (e.g., fair clauses, protections, etc.).  
  - Helps users see not only risks but also strengths in the contract.

- **Export analysis**  
  - Users can **export** the analysis (e.g., for sharing or saving offline).  
  - Export includes risk level and key points from the analysis.  
  - Export to PDF is supported for the analysis report.

- **Analysis history**  
  - Users can see how many PDF results have been generated.  
  - A history list of previous uploads and their risk levels.  
  - Users can delete saved analysis data from the website when they no longer need it.

---

## Tech Stack

- **Frontend**
  - HTML, CSS, TypeScript  
  - **Tailwind CSS** for styling and theming  
  - JSON data structures for handling contract analysis results

- **Backend / Services**
  - **Supabase**
    - Auth: user sign up / login  
    - Database: storing user records, contract metadata, and analysis history  
    - (Optionally) Storage: for storing uploaded PDF files

- **Deployment / Environment**
  - Currently running on **localhost** for development  
  - Can be deployed to Vercel, Netlify, or any static hosting with a Supabase backend

---

## Project Structure (High Level)

> This is a simplified overview; adjust to match your exact folders if needed.

- `/src` – main frontend code (TypeScript, components, pages)  
- `/images` – static assets (logos, screenshots, etc.)  
- `/public` – public assets (favicon, robots.txt, placeholders)  
- `/supabase` – Supabase configuration, migrations, and edge functions  
- `tailwind.config.js` – Tailwind CSS configuration  
- `index.html` – main HTML entry file  
- `package.json` – scripts and dependencies

---

## Getting Started (Local Development)

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/contract-risk-analyzer.git
   cd contract-risk-analyzer
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up Supabase**

   - Create a project at <https://supabase.com>.  
   - Set up:
     - Auth (Email/password)  
     - Database tables for users, contracts, and analysis history.  
   - Create a `.env` or `.env.local` file with your Supabase keys, for example:

     ```bash
     VITE_SUPABASE_URL=your-supabase-url
     VITE_SUPABASE_ANON_KEY=your-supabase-anon-key
     ```

4. **Run the development server**

   ```bash
   npm run dev
   ```

5. **Open the app**

   - Go to `http://localhost:5173` (or the port shown in your terminal when Vite starts).

---

## Future Improvements

- Replace placeholder analysis logic with a **real AI model** (e.g., Gemini or OpenAI) for deeper contract understanding.  
- Add more detailed clause categories (liability, termination, confidentiality, payment terms, IP, governing law, etc.).  
- Add role‑based access for advanced features (e.g., admin vs regular users).  
- Deploy to a public URL (Vercel / Netlify) and use a production Supabase project.  

---

## Status

- ✅ Core features working on localhost  
- ✅ Analysis engine fetches text data from the PDF and generates suggestions based on risk level  
- ✅ Export to PDF option available for the analysis report  
- ✅ History of user data/files, with the ability for users to delete saved data  
- 🚧 Can be upgraded with a custom AI prompt or more advanced backend logic for better contract understanding
