# वनLIFE

### AI-Powered Wildlife Protection & Response Platform

[![Live Demo](https://img.shields.io/badge/Live-Demo-brightgreen)](https://one-life-waox.vercel.app/)
[![Frontend](https://img.shields.io/badge/Frontend-Vercel-black)](https://vercel.com/)
[![Backend](https://img.shields.io/badge/Backend-Render-blue)](https://render.com/)

**वनLIFE** is an AI-powered wildlife protection platform that transforms citizen reports into actionable intelligence through camera + GPS reporting, AI-assisted triage, explainable risk prioritization, protected location intelligence, and officer-driven response.

Built for **Infinity Hacks 2026**.

---

## 🚀 Live Demo

**Try वनLIFE:**
https://one-life-waox.vercel.app/

**Backend API:**
https://eco-guardian-api.onrender.com

---

## 🎯 Problem

Wildlife incidents are often reported with incomplete information, delayed response, and limited coordination between citizens and field officers.

वनLIFE addresses this by creating a structured pipeline:

```text
Citizen Report
      ↓
Camera + GPS Evidence
      ↓
AI-Assisted Assessment
      ↓
Risk & Priority Analysis
      ↓
Officer Intelligence Dashboard
      ↓
Response Unit Recommendation
      ↓
Dispatch & Response
```

The platform is designed to turn raw citizen observations into structured, actionable intelligence while protecting sensitive wildlife locations from public exposure.

---

# ✨ Key Features

## 👤 Citizen Platform

* Citizen registration and login
* Role-based access
* Citizen profile
* My Reports dashboard
* Wildlife incident reporting
* Incident category selection
* Live browser camera capture
* GPS location capture
* Latitude, longitude and accuracy information
* Review & Submit workflow
* AI assessment results
* Report status tracking

---

## 🤖 AI-Assisted Assessment

वनLIFE uses **Gemini and OpenAI** to assist with wildlife incident assessment.

The system can provide:

* Species analysis
* Incident type classification
* Severity assessment
* Confidence estimation
* Explainable AI reasoning
* Recommended action
* Risk score
* Risk-factor visualization

The goal is not simply to generate an AI prediction, but to turn the assessment into information that can support operational decision-making.

---

## 🗺️ Public Wildlife Intelligence Explorer

A public-facing intelligence layer allows users to explore wildlife activity without exposing sensitive exact locations.

Features include:

* Interactive wildlife map
* Public-safe/coarse location masking
* Incident category filters
* 24H / 7D / 30D time filters
* Search by species
* Search by region
* Search by incident type
* Interactive intelligence feed
* Map markers
* Newly reported incident integration
* Light / Forest map themes

### Location Protection

Exact wildlife incident coordinates are **not exposed publicly**.

The public interface uses coarse/safe location visualization, while authorized officers can access exact operational locations.

---

# 🛡️ Officer Operations

Protected officer functionality provides operational intelligence for responding to incidents.

Features include:

* Officer registration
* Pending officer verification
* Protected officer login
* Risk-prioritized incident queue
* Incident detail view
* Exact-location map
* Incident status management
* Nearest response-unit lookup
* Response-unit availability
* Recommended response unit
* Estimated response time
* SOS dispatch workflow
* Dispatch confirmation
* Response timeline

### Dispatch States

```text
Ready
  ↓
Dispatching
  ↓
Dispatched
```

The system also generates dispatch references for tracking response operations.

---

# 🚨 SOS & Response

वनLIFE includes an SOS-driven response workflow designed for urgent wildlife situations.

The platform can:

1. Identify a high-priority incident
2. Analyze available response units
3. Calculate distance using the Haversine formula
4. Recommend an appropriate response unit
5. Estimate response time
6. Initiate dispatch
7. Track dispatch status
8. Maintain a response timeline

---

# 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │      Citizens       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   React Frontend    │
                    │ TypeScript + Vite   │
                    └──────────┬──────────┘
                               │
                    REST API / Authentication
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Django Backend    │
                    │ Django REST API     │
                    └──────────┬──────────┘
                               │
          ┌────────────────────┼────────────────────┐
          │                    │                    │
          ▼                    ▼                    ▼
   PostgreSQL DB        AI Services          Image Storage
                       Gemini + OpenAI       Cloudinary / S3
          │
          │
          ▼
 ┌─────────────────────┐
 │ Officer Operations  │
 │      Dashboard      │
 └──────────┬──────────┘
            │
            ▼
   Response Unit / SOS
```

---

# 🛠️ Technology Stack

## Frontend

* React
* TypeScript
* Vite
* Tailwind CSS
* Leaflet
* React-Leaflet
* Native MediaDevices API
* Native Geolocation API
* Canvas API
* React Context API
* LocalStorage / SessionStorage
* HTML5
* CSS3

## Backend

* Django
* Django REST Framework
* PostgreSQL
* Session / Token Authentication
* Role-Based Access Control (RBAC)
* Gemini
* OpenAI
* Haversine distance calculation
* Cloudinary / S3
* Twilio
* Environment variables

## Deployment

* **Frontend:** Vercel
* **Backend:** Render
* **Database:** PostgreSQL

---

# 📱 User Roles

## Citizen

Citizens can:

* Create an account
* Report wildlife incidents
* Capture photographic evidence
* Share GPS information
* Review and submit reports
* View AI assessment
* Track report status
* Explore public wildlife intelligence

## Officer

Officers can:

* Register and undergo verification
* Access protected operational information
* View prioritized incidents
* Access exact incident locations
* Manage incident status
* Find nearby response units
* Initiate SOS dispatch
* Track response operations

## Admin

Administrators provide platform-level management and control over the system.

---

# 🔐 Security & Privacy

वनLIFE separates public intelligence from protected operational information.

Key principles include:

* Role-based access control
* Protected citizen/officer routes
* Authentication-based access
* Public-safe location masking
* Exact coordinates restricted to authorized operational users
* Environment variables for sensitive configuration
* Separate public and protected navigation flows

---

# 📊 Risk Prioritization

Incidents are analyzed and prioritized using multiple factors.

The platform combines AI-assisted assessment with operational information to help officers understand:

* Severity
* Confidence
* Incident type
* Species
* Location
* Risk factors
* Response requirements

This allows officers to focus on incidents requiring the most urgent attention.

---

# 📍 Geospatial Intelligence

વનLIFE uses geospatial information throughout the reporting and response workflow.

The platform captures:

```text
Latitude
Longitude
Accuracy
```

For operational response, the system uses the **Haversine distance formula** to calculate the distance between an incident and available response units.

This supports:

* Nearest-unit identification
* Response-unit recommendation
* Distance calculation
* Estimated response time
* Operational dispatch

---

# 🎨 UI / UX

વનLIFE follows a cinematic wildlife-focused design language.

The interface is designed for both desktop and mobile devices and includes:

* Responsive layouts
* Wildlife-focused visual design
* Cinematic landing page
* Interactive maps
* Forest-themed map mode
* Light map mode
* Clear operational dashboards
* Risk visualization
* Mobile-friendly reporting workflow

---

# ⚙️ Basic Local Setup

## Frontend

```bash
cd frontend
npm install
npm run dev
```

The frontend will run locally using Vite.

## Backend

```bash
cd eco_guardian
pip install -r requirements.txt
python manage.py runserver
```

The Django backend will start locally.

> Environment variables and database configuration are required for full local functionality.

---

# 🌐 Deployment

### Frontend

The React frontend is deployed using **Vercel**.

### Backend

The Django REST API is deployed using **Render**.

### Production Flow

```text
GitHub
   │
   ├──────────────► Vercel
   │                  │
   │                  ▼
   │             React Frontend
   │                  │
   │                  ▼
   └──────────────► Render
                      │
                      ▼
                 Django REST API
                      │
          ┌───────────┼───────────┐
          ▼           ▼           ▼
      PostgreSQL     AI       Storage/SOS
                   Services
```

---

# 👨‍💻 Contributions

## Frontend — Anish Kumar Rai

Responsible for the frontend development and overall visual direction of वनLIFE, including:

* UI/UX design
* Overall वनLIFE visual direction
* Cinematic landing page and hero section
* React + TypeScript component development
* Citizen authentication screens
* Citizen profile and My Reports
* Complete citizen incident reporting workflow
* Browser camera integration
* GPS integration
* Review & Submit workflow
* AI assessment result interface
* Public Wildlife Intelligence Explorer
* Interactive Leaflet maps
* Public-safe location visualization
* Officer authentication screens
* Officer Operations Dashboard
* Officer incident detail interface
* Exact-location map
* Risk and priority visualization
* Response-unit lookup interface
* SOS / dispatch workflow UI
* Route protection and authentication flows
* Responsive desktop and mobile interface
* Frontend state management
* API/service abstraction
* Django REST API integration preparation

## Backend — Teammate

Responsible for the backend implementation, including:

* Django backend
* Django REST Framework APIs
* PostgreSQL database
* Authentication and RBAC
* AI service integration
* Incident processing
* Risk assessment
* Response-unit logic
* Image storage integration
* SOS notification functionality
* Backend deployment and integration

---

# 🏆 Hackathon

**Infinity Hacks 2026**

वनLIFE was developed as a hackathon project focused on combining **AI, geospatial intelligence, citizen participation, and emergency response** for wildlife protection.

---

# 🔮 Future Improvements

Potential future enhancements include:

* Real-time officer notifications
* Advanced wildlife species recognition
* Historical incident trend analysis
* Wildlife corridor intelligence
* Offline-first incident reporting
* Automated escalation for critical incidents
* Advanced predictive risk modelling
* Integration with government wildlife departments
* IoT camera and sensor integration
* Real-time response-unit tracking

---

# 📌 Project Status

**Status:** Deployed & Functional

### Live Application

https://one-life-waox.vercel.app/

### Repository

https://github.com/anish113356-ship-it/-LIFE

---

## 🌿 वनLIFE

**From citizen observation to actionable wildlife intelligence.**
