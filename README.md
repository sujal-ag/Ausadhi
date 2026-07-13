# Ausadhi — Healthcare Appointment Platform

## Repositories
- 🖥️ [Frontend](https://github.com/sujal-ag/Ausadhi-frontend)
- ⚙️ [Backend](https://github.com/sujal-ag/Ausadhi-backend)
- 🛠️ [Admin](https://github.com/sujal-ag/Ausadhi-admin)

## Live
[ausadhi.in](https://ausadhi.in)

## About

Ausadhi is a full-stack healthcare appointment platform I designed, built, 
and deployed independently — from database schema to production server. 
It's a complete web application for booking appointments, with WhatsApp 
as an additional booking channel, AI-based symptom triage, integrated 
payments, and automated reminders — plus a separate admin dashboard for 
clinic staff.

Rather than using a no-code/PaaS shortcut, I built and self-hosted the 
entire stack — frontend, API, automation layer, and infrastructure — to 
get hands-on with the kind of systems used in production environments.

## What It Does

- **Web Booking** — Patients can browse doctor availability and book 
  appointments directly through the website (ausadhi.in)
- **WhatsApp Booking** — Alternate booking flow via WhatsApp (built with 
  n8n + WhatsApp Business API) for patients who prefer messaging over 
  the web
- **AI Triage** — Ayu, an LLM-based chatbot, collects basic symptom info 
  before the visit and shares a summary with clinic staff
- **Payments** — Razorpay integration handles consultation fees end-to-end 
  (checkout, webhooks, verification)
- **Reminders** — Automated email reminders (via Resend) reduce no-shows
- **Admin Dashboard** — Internal tool for clinic staff to manage bookings 
  and patient records

## Architecture & Technical Decisions

- **Frontend** (React) — full patient-facing web app for browsing doctors, 
  booking, and payments
- **Backend** (Node.js + MongoDB Atlas) — REST API for bookings, schedules, 
  patient records, and payment webhooks
- **Automation Layer** (n8n) — powers the WhatsApp booking flow and 
  triggers reminder workflows asynchronously
- **Infrastructure** — Dockerized services on an Azure VM, Nginx as reverse 
  proxy with SSL, custom domain + DNS configuration

Chose to self-host on a VM (instead of Vercel/Render) specifically to work 
with Docker, Nginx, and server-level networking/DNS — closer to how 
infra is actually managed at most companies.

## Tech Stack
React · Node.js · MongoDB Atlas · Docker · Nginx · n8n · Razorpay · 
WhatsApp Business API · Resend
