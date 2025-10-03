# SensAI — AI-Powered Career Coach

**Description**  
SensAI is an AI-driven career coaching platform that helps users generate optimized resumes and cover letters, practice mock interviews, and receive weekly career/market insights. This repository contains the project documentation and presentation (with system diagrams, data models, and UI screenshots).

---

## Status
**Documentation & design only** — This repo currently contains project documentation and the final presentation PDF. The runnable code is not included due to environment/dependency constraints (Gemini API, NeonDB, etc.).

---

## Table of Contents
- [Project Summary](#project-summary)  
- [Core Features](#core-features)  
- [Tech Stack](#tech-stack)  
- [Architecture & Documentation](#architecture--documentation)  
- [Data Model (summary)](#data-model-summary)  
- [Screenshots & UI](#screenshots--ui)  
- [Contributions & My Role](#contributions--my-role)  
- [Future Work & Limitations](#future-work--limitations)  
- [References](#references)  
- [License](#license)  

---

## Project Summary
SensAI streamlines job hunting by generating polished, ATS-friendly resumes and cover letters, generating mock interview questions, and delivering weekly career insights tailored by industry. The platform is designed for students and professionals seeking personalized, fast, and affordable career coaching.

---

## Core Features
- AI Resume Builder (customized resume generation)  
- Cover Letter Generator (tailored to job description/company)  
- Mock Interview Generator & Scoring (generate Q&A + basic scoring)  
- Weekly Career & Industry Insights (scheduled background jobs)  
- Secure Authentication & User Profiles  
- **Stripe Payment Gateway Integration (credit/payment system)**  
- Team collaboration and documentation support  

---

## Tech Stack
**Frontend**  
- Next.js + React.js  
- Tailwind CSS, shadcn/ui (UI components)

**Backend / DevOps**  
- Node.js, Express.js  
- Prisma ORM (data modeling)  
- Neon (PostgreSQL) as DB  
- Inngest (background jobs / scheduled insights)  
- Clerk (authentication)  
- **Stripe (payments / credits)**  
- Gemini AI (AI generation API)

---

## Architecture & Documentation
This repository includes the **full project presentation** with:  
- System diagrams  
- Data flow diagrams  
- Sequence diagrams  
- Entity Relationship Diagram (ERD)  
- UI screenshots  

📄 [Project Presentation (PDF)](docs/sensai-presentation.pdf)

---

## Data Model (summary)
Main entities:  
- **User**: `id`, `email`, `name`, `imageUrl`, `industry`, `skills[]`, `createdAt`, `updatedAt`  
- **Resume**: `id`, `userId`, `content`, `createdAt`, `updatedAt`  
- **CoverLetter**: `id`, `userId`, `content`, `companyName`, `jobTitle`, `createdAt`, `updatedAt`  
- **Assessment**: `id`, `userId`, `quizScore`, `questions[]`, `improvementTip`, `createdAt`  
- **IndustryInsight**: `id`, `industry`, `salaryRanges`, `growthRate`, `topSkills[]`, `lastUpdated`

(Full details and diagrams inside the presentation PDF.)

---

## Screenshots & UI
UI screenshots are included in the **presentation PDF** under `/docs/`.  
They showcase:  
- Landing / Dashboard  
- Resume Builder  
- Mock Interview  
- Career Insights  

---

## Contributions & My Role
This was a 4-member team project. My key contributions included:

- **Backend Development**: Implemented core REST APIs in Express.js, integrated NeonDB via Prisma ORM, and set up authentication & authorization.  
- **Payment Integration**: Successfully integrated **Stripe Payment Gateway** for credit/payment flow.  
- **Frontend Work**: Built and styled resume builder and insights dashboard using React.js + Tailwind CSS.  
- **Documentation & Presentation**: Co-prepared system diagrams, data models, and final project presentation. 

---

## Future Work & Limitations
**Limitations (current repo)**: code not public due to environment & API keys; repo contains documentation only.  
**Future work**: Job recommendation engine, mobile app, multilingual support, recorded video interview analysis, and full code release with sanitized environment variables.

---

## References
- Next.js, Tailwind, Prisma, Neon, Inngest, Stripe, Gemini API  
(Reference list compiled from the project presentation.)

---

## License
MIT © Afshin Pathan
