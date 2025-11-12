# Technology Stack - Cloud Web Hosting Platform

**Version:** 1.0  
**Last Updated:** 2025-11-12  
**Owner:** @techfixind  

---

## Table of Contents

1. [Frontend Stack](#frontend-stack)
2. [Backend Stack](#backend-stack)
3. [Database & Storage](#database--storage)
4. [Infrastructure & DevOps](#infrastructure--devops)
5. [Security & Authentication](#security--authentication)
6. [Monitoring & Logging](#monitoring--logging)
7. [AI & Machine Learning](#ai--machine-learning)
8. [Third-Party Integrations](#third-party-integrations)
9. [Development Tools](#development-tools)
10. [Version Policy](#version-policy)

---

## Frontend Stack

### Core Framework & Libraries

| Technology | Version | Purpose | Documentation |
|------------|---------|---------|---------------|
| **React** | 18.3+ | UI library | https://react.dev |
| **TypeScript** | 5.5+ | Type safety | https://www.typescriptlang.org |
| **Vite** | 5.4+ | Build tool (replaces CRA) | https://vitejs.dev |
| **Material-UI (MUI)** | 6.1+ | Component library | https://mui.com |
| **React Router** | 6.26+ | Client-side routing | https://reactrouter.com |

### State Management & Data Fetching

| Technology | Version | Purpose |
|------------|---------|---------|
| **Zustand** | 4.5+ | Global state management (lightweight alternative to Redux) |
| **TanStack Query (React Query)** | 5.56+ | Server state management, caching, data fetching |
| **Axios** | 1.7+ | HTTP client with interceptors |

### Forms & Validation

| Technology | Version | Purpose |
|------------|---------|---------|
| **React Hook Form** | 7.53+ | Form state management |
| **Zod** | 3.23+ | Schema validation (TypeScript-first) |

### UI/UX Libraries

| Technology | Version | Purpose |
|------------|---------|---------|
| **Emotion** | 11.13+ | CSS-in-JS (used by MUI) |
| **Recharts** | 2.12+ | Charts and data visualization |
| **date-fns** | 3.6+ | Date manipulation |
| **react-dropzone** | 14.2+ | File upload component |
| **react-toastify** | 10.0+ | Toast notifications |
| **framer-motion** | 11.5+ | Animations |

### Code Editor & File Manager

| Technology | Version | Purpose |
|------------|---------|---------|
| **Monaco Editor** | 0.51+ | In-browser code editor (VS Code's editor) |
| **react-filemanager** | Custom | File manager UI component |

### Build & Bundling

| Technology | Version | Purpose |
|------------|---------|---------|
| **Vite** | 5.4+ | Dev server & bundler (fast HMR) |
| **ESBuild** | 0.23+ | JavaScript bundler (used by Vite) |
| **PostCSS** | 8.4+ | CSS transformations |
| **Autoprefixer** | 10.4+ | CSS vendor prefixing |

### Testing

| Technology | Version | Purpose |
|------------|---------|---------|
| **Vitest** | 2.1+ | Unit testing (Vite-native) |
| **React Testing Library** | 16.0+ | Component testing |
| **Playwright** | 1.47+ | E2E testing |
| **MSW (Mock Service Worker)** | 2.4+ | API mocking |

---

## Backend Stack

### Node.js Backend

| Technology | Version | Purpose |
|------------|---------|---------|
| **Node.js** | 22 LTS | JavaScript runtime |
| **TypeScript** | 5.5+ | Type safety |
| **Fastify** | 4.28+ | Web framework (2x faster than Express) |
| **Prisma** | 5.20+ | ORM for PostgreSQL |
| **Zod** | 3.23+ | Request/response validation |

### ASP.NET Backend (Windows)

| Technology | Version | Purpose |
|------------|---------|---------|
| **ASP.NET Core** | 8.0 LTS | Web framework |
| **C#** | 12 | Programming language |
| **Entity Framework Core** | 8.0+ | ORM for MSSQL/PostgreSQL |
| **FluentValidation** | 11.9+ | Request validation |

### API & Authentication

| Technology | Version | Purpose |
|------------|---------|---------|
| **Fastify JWT** | 8.0+ | JWT generation & validation |
| **node-oauth2-server** | 4.0+ | OAuth 2.0 server |
| **speakeasy** | 2.0+ | TOTP (2FA) generation |
| **argon2** | 0.40+ | Password hashing (more secure than bcrypt) |

### Background Jobs & Queues

| Technology | Version | Purpose |
|------------|---------|---------|
| **BullMQ** | 5.13+ | Redis-backed job queue |
| **node-cron** | 3.0+ | Scheduled tasks (cron jobs) |

### Email & Notifications

| Technology | Version | Purpose |
|------------|---------|---------|
| **Nodemailer** | 6.9+ | Email sending (SMTP) |
| **Handlebars** | 4.7+ | Email template engine |
| **Twilio SDK** | 5.3+ | SMS notifications |

### API Documentation

| Technology | Version | Purpose |
|------------|---------|---------|
| **OpenAPI (Swagger)** | 3.1 | API specification |
| **Fastify Swagger** | 8.15+ | Auto-generate Swagger docs |
| **Redoc** | 2.1 | Beautiful API documentation UI |

---

## Database & Storage

### Primary Database

| Technology | Version | Purpose | Notes |
|------------|---------|---------|-------|
| **PostgreSQL** | 16+ | Relational database | Multi-tenant with row-level security (RLS) |
| **Prisma** | 5.20+ | ORM & migrations | Type-safe database access |

**Extensions:**
- `pg_trgm` - Full-text search
- `uuid-ossp` - UUID generation
- `pgcrypto` - Encryption functions

### Caching & Session Store

| Technology | Version | Purpose |
|------------|---------|---------|
| **Redis** | 7.2+ | Cache, sessions, job queues |
| **ioredis** | 5.4+ | Redis client for Node.js |

### Analytics Database

| Technology | Version | Purpose |
|------------|---------|---------|
| **ClickHouse** | 24.8+ | OLAP database for logs & analytics |

### Object Storage

| Technology | Version | Purpose |
|------------|---------|---------|
| **MinIO** | Latest | S3-compatible object storage (self-hosted) |
| **AWS S3** | N/A | Cloud object storage (offsite backups) |

### File Storage

| Technology | Purpose |
|------------|---------|
| **NFS** | Network file system (Linux shared storage) |
| **CIFS/SMB** | Windows shared storage |

---

## Infrastructure & DevOps

### Containerization & Orchestration

| Technology | Version | Purpose |
|------------|---------|---------|
| **Docker** | 25+ | Container runtime |
| **Docker Compose** | 2.29+ | Multi-container orchestration (customer websites) |
| **Kubernetes (K8s)** | 1.30+ | Container orchestration (platform services) |
| **Helm** | 3.16+ | Kubernetes package manager |

### Infrastructure as Code (IaC)

| Technology | Version | Purpose |
|------------|---------|---------|
| **Terraform** | 1.9+ | Provision infrastructure (servers, networks, storage) |
| **Ansible** | 2.17+ | Configuration management (install packages, configure services) |
| **cloud-init** | Latest | Initial server setup (Ubuntu) |

### CI/CD

| Technology | Version | Purpose |
|------------|---------|---------|
| **GitHub Actions** | N/A | CI/CD pipelines |
| **Docker Registry** | N/A | GitHub Container Registry (ghcr.io) |
| **ArgoCD** | 2.12+ | GitOps for Kubernetes deployments |

### Load Balancing & Reverse Proxy

| Technology | Version | Purpose |
|------------|---------|---------|
| **NGINX** | 1.27+ | Reverse proxy, load balancer, SSL termination |
| **HAProxy** | 2.9+ | Alternative load balancer (if needed) |

### DNS

| Technology | Version | Purpose |
|------------|---------|---------|
| **PowerDNS** | 4.9+ | Authoritative DNS server with API |
| **Cloudflare** | N/A | DNS + CDN + DDoS protection |

### SSL/TLS

| Technology | Version | Purpose |
|------------|---------|---------|
| **Let's Encrypt** | N/A | Free SSL certificates |
| **acme.sh** | 3.0+ | ACME client (automated SSL) |
| **Certbot** | 2.11+ | Alternative ACME client |

---

## Security & Authentication

### Authentication & Authorization

| Technology | Version | Purpose |
|------------|---------|---------|
| **OAuth 2.0** | RFC 6749 | Authorization framework |
| **JWT (JSON Web Tokens)** | RFC 7519 | Stateless authentication |
| **TOTP (Time-based OTP)** | RFC 6238 | Two-factor authentication |
| **speakeasy** | 2.0+ | TOTP library |

### Encryption

| Technology | Purpose |
|------------|---------|
| **TLS 1.3** | Transport layer security (HTTPS) |
| **AES-256** | Data encryption at rest |
| **argon2** | Password hashing |
| **LUKS** | Linux disk encryption |
| **BitLocker** | Windows disk encryption |

### Security Tools

| Technology | Version | Purpose |
|------------|---------|---------|
| **fail2ban** | 1.1+ | Intrusion prevention (ban IPs after failed logins) |
| **ClamAV** | 1.3+ | Antivirus scanner |
| **OSSEC / Wazuh** | 4.9+ | Host-based intrusion detection (HIDS) |
| **Trivy** | 0.55+ | Container vulnerability scanner |
| **Snyk** | Latest | Dependency vulnerability scanning |

### Secrets Management

| Technology | Version | Purpose |
|------------|---------|---------|
| **HashiCorp Vault** | 1.17+ | Secrets management (passwords, API keys) |
| **dotenv-vault** | 1.26+ | Encrypted .env files |

---

## Monitoring & Logging

### Metrics & Monitoring

| Technology | Version | Purpose |
|------------|---------|---------|
| **Prometheus** | 2.54+ | Metrics collection & storage |
| **Grafana** | 11.2+ | Metrics visualization & dashboards |
| **Node Exporter** | 1.8+ | Server metrics (CPU, RAM, disk) |
| **cAdvisor** | 0.49+ | Container metrics |
| **PostgreSQL Exporter** | 0.15+ | PostgreSQL metrics |
| **Redis Exporter** | 1.62+ | Redis metrics |

### Logging

| Technology | Version | Purpose |
|------------|---------|---------|
| **Loki** | 3.1+ | Log aggregation (Prometheus for logs) |
| **Promtail** | 3.1+ | Log shipper (sends logs to Loki) |
| **Pino** | 9.4+ | Structured logging for Node.js |
| **Serilog** | 4.0+ | Structured logging for ASP.NET Core |

### Tracing

| Technology | Version | Purpose |
|------------|---------|---------|
| **Jaeger** | 1.60+ | Distributed tracing |
| **OpenTelemetry** | 1.26+ | Observability framework (traces, metrics, logs) |

### Alerting

| Technology | Version | Purpose |
|------------|---------|---------|
| **Alertmanager** | 0.27+ | Alert routing (Prometheus alerts) |
| **PagerDuty** | N/A | On-call management & incident response |

### Uptime Monitoring

| Technology | Purpose |
|------------|---------|
| **UptimeRobot** | External uptime monitoring (free tier) |
| **Pingdom** | Alternative uptime monitoring |

---

## AI & Machine Learning

### AI APIs

| Technology | Version | Purpose |
|------------|---------|---------|
| **OpenAI API** | GPT-4o | AI assistant, auto-troubleshooting, security advisor |
| **Azure OpenAI** | GPT-4 | Alternative (for compliance, data residency) |

### AI Orchestration

| Technology | Version | Purpose |
|------------|---------|---------|
| **LangChain** | 0.3+ | AI workflow orchestration |
| **LangSmith** | Latest | LangChain monitoring & debugging |

### Vector Database (RAG)

| Technology | Version | Purpose |
|------------|---------|---------|
| **Pinecone** | N/A | Vector database for RAG (Retrieval-Augmented Generation) |
| **Weaviate** | 1.26+ | Open-source vector database (alternative) |

### Machine Learning (Churn Prediction)

| Technology | Version | Purpose |
|------------|---------|---------|
| **scikit-learn** | 1.5+ | ML library (Python) |
| **pandas** | 2.2+ | Data manipulation |
| **NumPy** | 2.1+ | Numerical computing |
| **FastAPI** | 0.115+ | Python API for ML models |

---

## Third-Party Integrations

### Payment Gateways

| Provider | SDK Version | Purpose |
|----------|-------------|---------|
| **Razorpay** | 2.9+ (Node.js) | Payment processing (India, GST support) |
| **Stripe** | 16.12+ (Node.js) | International payments |

### Email Service Providers

| Provider | SDK Version | Purpose |
|----------|-------------|---------|
| **Amazon SES** | AWS SDK 3.x | Transactional emails (high volume) |
| **SendGrid** | 7.7+ | Alternative email service |

### SMS Providers

| Provider | SDK Version | Purpose |
|----------|-------------|---------|
| **Twilio** | 5.3+ | SMS notifications (international) |
| **MSG91** | Latest | SMS notifications (India-focused) |

### CDN

| Provider | Purpose |
|----------|---------|
| **Cloudflare** | CDN, DDoS protection, DNS |
| **BunnyCDN** | Alternative CDN (cost-effective) |

---

## Development Tools

### Monorepo Management

| Technology | Version | Purpose |
|------------|---------|---------|
| **Turborepo** | 2.1+ | Monorepo build system (caching, parallel builds) |
| **pnpm** | 9.11+ | Fast, disk-efficient package manager |

### Code Quality

| Technology | Version | Purpose |
|------------|---------|---------|
| **ESLint** | 9.11+ | JavaScript/TypeScript linting |
| **Prettier** | 3.3+ | Code formatting |
| **Husky** | 9.1+ | Git hooks (pre-commit, pre-push) |
| **lint-staged** | 15.2+ | Run linters on staged files |

### Git

| Technology | Version | Purpose |
|------------|---------|---------|
| **Git** | 2.46+ | Version control |
| **Conventional Commits** | N/A | Commit message standard |
| **Semantic Release** | 24.1+ | Automated versioning & changelog |

### IDE & Extensions

| Tool | Purpose |
|------|---------|
| **VS Code** | Primary IDE |
| **GitHub Copilot** | AI pair programmer |
| **Prettier Extension** | Auto-formatting |
| **ESLint Extension** | Real-time linting |
| **Prisma Extension** | Database schema IntelliSense |

---

## Version Policy

### Update Strategy

1. **Immediate Updates:**
   - Security patches (CVEs)
   - Critical bug fixes

2. **Monthly Updates:**
   - Minor version updates (e.g., 5.1 → 5.2)
   - Non-breaking dependency updates

3. **Quarterly Updates:**
   - Major version updates (e.g., 5.x → 6.x)
   - Framework upgrades (React, Node.js LTS)

4. **Annual Updates:**
   - OS upgrades (Ubuntu LTS releases)
   - Database major versions

### Testing Before Updates

- **Development:** Test in dev environment (1 week)
- **Staging:** Test in staging environment (1 week)
- **Production:** Canary deployment (10% traffic, 3 days) → full rollout

### Deprecation Policy

- **6 months notice** before removing support for a major version
- **Automated migration scripts** for breaking changes

---

## Technology Decision Criteria

When evaluating new technologies, we consider:

1. **Maturity:** Stable, production-ready (avoid alpha/beta)
2. **Community:** Active maintenance, large community, good documentation
3. **Performance:** Benchmarks, resource efficiency
4. **Security:** CVE track record, security best practices
5. **License:** OSS-friendly (MIT, Apache 2.0, BSD)
6. **Team Expertise:** Learning curve, training availability
7. **Vendor Lock-in:** Avoid proprietary solutions where possible

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-12 | @techfixind | Initial technology stack documentation |

---

**Next:** [FEATURES.md](FEATURES.md) - Complete feature specifications
