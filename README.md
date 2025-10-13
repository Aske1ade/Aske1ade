<div align="center">

# Hi, I'm **Aliar** 👋

**Full‑Stack Engineer** · Next.js / React · Tailwind · FastAPI · PostgreSQL · Docker · DevOps basics
Building clean, production‑ready web apps and marketplaces.

[![Telegram](https://img.shields.io/badge/Telegram-@lunarisamator-26A5E4?style=for-the-badge\&logo=telegram\&logoColor=white)](https://t.me/lunarisamator)
[![Email](https://img.shields.io/badge/Email-aliar8004@gmail.com-D14836?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:aliar8004@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Askelade-0A66C2?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://www.linkedin.com/in/askelade/)

</div>

---

## 📌 Profile README (Overview)

* 🔭 Currently building **GoCart** — an open‑source multi‑vendor e‑commerce platform (Next.js + Tailwind + Redux Toolkit; optional FastAPI + PostgreSQL; S3/MinIO for media).
* 🎓 Thesis side‑project: **Restaurant Booking Platform** for large events in Kazakhstan.
* 🛰 Networking & monitoring background: **MikroTik**, Grafana, Zabbix; interested in on‑prem **LLM/ASR** pipelines.
* ⚙️ Favorite patterns: clean architecture, role‑based access, typed API contracts, CI/CD.
* 🌍 Location: Almaty/Astana, Kazakhstan.


---

## 🧬 Bio

I’m **Azimsham Aliar**, a full‑stack developer who enjoys shipping pragmatic, reliable products.
On the frontend I value minimal, accessible UI and predictable state; on the backend — clear module boundaries, stable contracts, and observability.
I build marketplaces, admin dashboards, and real‑time integrations, aiming for production readiness from day one.

**Now**: improving performance and DX, and experimenting with local AI services (LLM/ASR) without sending data to external clouds.

---

## 🛠️ Tech Stack

**Frontend**: Next.js, React, Tailwind CSS, Redux Toolkit, React Hook Form
**Backend**: FastAPI, Node.js (API routes), REST/JSON, Webhooks
**Data**: PostgreSQL (Prisma/SQL), Redis (cache)
**Storage**: S3/MinIO (image uploads, signed URLs)
**Auth**: NextAuth (Email/OAuth/credentials), RBAC (admin/vendor/customer)
**DevOps**: Docker, docker‑compose, Nginx, basic CI/CD
**Monitoring**: Grafana, Zabbix
**Networking**: MikroTik

> Also familiar with: Stripe/Kaspi payments, Playwright/Jest/Vitest, GitHub Actions.

---

## 🧭 Highlights

- **GoCart (Multi-Vendor Marketplace)**  
  Production-ready marketplace on Next.js + Tailwind + Redux Toolkit with **RBAC** (admin/vendor/customer), **NextAuth**, image storage via **S3/MinIO**, and pluggable payments (Stripe/Kaspi/Mock). Server-rendered (SSR/ISR), clean UI, vendor dashboards, admin controls, webhooks, and audit basics.

- **Restaurant Booking App**  
  Platform to **search & book venues** for large events (weddings, corporate, anniversaries) in Kazakhstan. Availability calendar, pricing rules, request/approval flow, notifications (email), media via S3/MinIO, and admin moderation. Stack: Next.js, FastAPI, PostgreSQL, Docker.

- **Internal Admin & Analytics**  
  Unified admin panel for internal systems: **dashboards with charts**, role separation, filters, CSV export, and **audit logs** for sensitive actions. Emphasis on predictable UX, access control, and operational metrics. Tech: Next.js, React, charting libs, REST APIs.

- **Government CRM System**  
  Centralized CRM for public-sector operators: **case management**, ticket routing, role-based access, document links, and integrations with telephony/service desk. On-prem deployment, minimal external dependencies, **audit/compliance** focus, and clear SLA reporting.

- **Asterisk SIP Management**  
  Web tools around Asterisk PBX: **real-time call logs**, queue monitoring, basic IVR routing, recordings catalog, and operator statistics. REST hooks for future **ASR/analytics**, role-based views, and lightweight dashboards. Designed for on-prem use.

- **ML/Ops: Face Detection Pipeline**  
  On-prem inference pipeline for **face detection** (CPU/GPU) with REST API, batch jobs, and monitoring. Containerized deploy, versioned models, simple feature flags, and metrics for throughput/latency. Integrates with storage backends for uploads/results.

- **AI Agents for Video Generation**  
  Prompt-driven workflow to generate scripts, TTS, talking-head segments, and **B-roll assembly**. Modular steps (script → voice → lip-sync → edit), configurable via YAML/JSON, resumable jobs, and on-prem friendly to avoid data exfiltration. Good for explainers and docs.


## 💼 Experience & Education (short)

* **Engineer — Freedom Telecom**
  *Ops, monitoring, networking; supervisor: Toktarbayev Daniyar (Operations Engineer for RRL).*
* **Full‑Stack Engineer — NITEC (2024–2025)**
  *Linux, FastAPI, React.js, PostgreSQL, Docker, Nginx, Grafana, Zabbix, CI/CD basics.*
* **B.S. in Cybersecurity — Astana IT University** (Diploma expected ~3 months from 2025‑03‑22).
---

## 🐳 Docker Example (compose)

```yaml
version: "3.9"
services:
  web:
    build: .
    container_name: gocart-web
    ports:
      - "3000:3000"
    env_file: .env
    depends_on:
      - db
      - minio
    command: "npm run start"
  db:
    image: postgres:16
    environment:
      POSTGRES_DB: gocart
      POSTGRES_USER: user
      POSTGRES_PASSWORD: password
    ports:
      - "5432:5432"
    volumes:
      - pg:/var/lib/postgresql/data
  minio:
    image: minio/minio:latest
    command: server /data --console-address ":9001"
    environment:
      MINIO_ROOT_USER: minioadmin
      MINIO_ROOT_PASSWORD: minioadmin
    ports:
      - "9000:9000"
      - "9001:9001"
    volumes:
      - minio:/data
volumes:
  pg:
  minio:
```

---

## 🔐 .env (example)

```env
NEXT_PUBLIC_APP_NAME=GoCart
NEXT_PUBLIC_BASE_URL=http://localhost:3000
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=change_me
DATABASE_URL=postgresql://user:password@localhost:5432/gocart?schema=public
S3_ENDPOINT=http://localhost:9000
S3_ACCESS_KEY=minioadmin
S3_SECRET_KEY=minioadmin
S3_BUCKET=gocart
S3_REGION=us-east-1
S3_FORCE_PATH_STYLE=true
PAYMENT_PROVIDER=mock
SMTP_HOST=localhost
SMTP_PORT=1025
SMTP_FROM="GoCart <noreply@gocart.local>"
```

---

## 📊 GitHub Stats (auto)

> Update `USERNAME` in image URLs.

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=aske1ade\&show_icons=true\&theme=transparent)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=aske1ade\&layout=compact\&theme=transparent)

[![GitHub Streak](https://streak-stats.demolab.com?user=aske1ade\&theme=transparent)](https://git.io/streak-stats)

[![trophy](https://github-profile-trophy.vercel.app/?username=aske1ade\&theme=flat\&no-frame=true\&margin-w=10)](https://github.com/ryo-ma/github-profile-trophy)

</div>

---

## 🤝 Open Source & Contributions

* PRs are welcome — feel free to open issues and propose improvements.
* I value clear PR descriptions, small commits, and tests for critical paths.

---

## 📨 Contact

* GitHub: [https://github.com/USERNAME](https://github.com/Aske1ade)
* Telegram: [https://t.me/YOUR_HANDLE](https://t.me/lunarisamator)
* Email: [email@domain.kz](mailto:aliar8004@gmail.com)

> If you find something useful here, consider leaving a ⭐ — it really helps.
