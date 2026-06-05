# Placemark — Location Review App

> CS335 Software Engineering Group Project · Maynooth University · Microsoft Mentorship Programme

A social location review platform — think Letterboxd, but for real-world places. Users discover and share reviews of locations filtered through their social network, with geo-proximity notifications when friends have rated somewhere nearby.

## 🔐 My Role — Authentication & Backend
- Implemented **Microsoft Entra External ID** (PKCE OAuth 2.0 flow) for all user authentication
- Azure AD JWTs validated on every Spring Boot API request via a custom security filter
- **Zero password storage** — user identity is derived entirely from the Azure OID claim
- Auto-provisioning on first login — sign-up and sign-in are the same single flow
- Resolved live OAuth errors (AADSTS50011, AADSTS50020) during Microsoft demo preparation

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React Native (Expo) |
| Backend | Spring Boot REST API |
| Authentication | Microsoft Entra External ID (PKCE + JWT) |
| Database | PostgreSQL + PostGIS |
| File Storage | Azure Blob Storage |
| Hosting | Azure App Service |

## ✨ Key Features
- Social feed of friends' location reviews
- Geo-proximity push notifications using PostGIS `ST_DWithin` spatial queries
- Location search, rating, and review creation
- Secure token-based auth with no password column in the database

## 👥 Team
**Felix Elmido** (Auth & Backend) · Jack James (Database) · Jack Duffin · Joel VG · Joye Zhang · Hamed Adeniji  
**Mentors:** Dominic & Victor — Microsoft Ireland

## 📁 Structure
- `/backend` — Spring Boot REST API
- `/frontend` — React Native (Expo) mobile app
- `/database` — PostgreSQL schema + PostGIS setup
- `/docs` — Architecture docs and demo materials
- `/research` — Initial project research
