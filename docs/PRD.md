# AI Recipe Generator – PRD

## Project Overview
An AI-powered web application that generates creative recipes based on ingredients input by the user. Authenticated via magic link (email), it uses n8n workflows connected to OpenAI to return recipe suggestions. Built with Supabase, MongoDB, and deployed on Vercel.

---

## Problem Statement
Users often struggle to decide what to cook with available ingredients at home. This app solves that by providing instant, AI-generated recipe suggestions based on whatever ingredients the user has.

---

## Key Features

- 🔐 **Authentication**: Magic Link login via Supabase Auth
- 🥕 **Ingredient Input**: Users enter ingredients manually
- 🤖 **AI Recipe Generation**: n8n triggers OpenAI API to return recipes
- 📜 **Recipe Result Display**: Beautifully formatted title, ingredients, and steps
- 🧾 **Optional History**: Store previous recipes per user using Supabase or MongoDB
- 🌐 **Responsive UI**: Mobile-first with Tailwind CSS + Shadcn UI
- 🎨 **Polished UX**: Framer Motion for animations, smooth form transitions

---

## Technical Architecture

**Frontend:** Next.js + Tailwind + Shadcn UI  
**Backend:** Supabase Functions (optional), Custom `/api` routes  
**AI Logic:** n8n + OpenAI API  
**Database:** Supabase PostgreSQL (Auth + History), optional MongoDB for flexibility  
**Deployment:** Vercel CI/CD

---

## Flow Diagram

1. User logs in via email (magic link)
2. Inputs ingredients
3. Frontend hits `/api/generate-recipe`
4. Backend triggers n8n workflow
5. n8n calls OpenAI → generates a structured recipe
6. Backend receives recipe and returns to frontend
7. Frontend displays recipe in a clean UI

---

## API Routes (Planned)

/api/generate-recipe → POST  
Payload: `{ ingredients: ["egg", "onion"] }`  
Returns: `{ title, ingredients[], steps[], nutrition? }`

---

## Deliverables

- `/docs`: PRD, wireframes ✅  
- `/api`: Backend endpoint to connect to n8n  
- `/app`: UI with login, input form, and result display  
- `/ai`: Sample JSON, n8n workflow docs  
- Demo: Live deployment on Vercel  
- Docs + Loom walkthrough for final submission
