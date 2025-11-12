# Cloud Web Hosting Platform - Project Overview

**Project Name:** Cloud Web Hosting Platform  
**Project Code:** CHP-2025  
**Owner:** @techfixind  
**Start Date:** 2025-11-12  
**Target Launch:** Q4 2025  

---

## Executive Summary

A next-generation, multi-tenant cloud web hosting platform supporting both Linux and Windows (ASP.NET) hosting with AI-powered assistance, complete automation, and three distinct portals (Customer, Reseller, Admin).

### Vision Statement

Build a professional, autonomous, AI-assisted hosting control panel that competes with HestiaCP, cPanel, Plesk, and Hostinger by offering:
- **Dual OS Support:** Linux (LAMP/LEMP, Node.js, Python) + Windows (IIS, ASP.NET, MSSQL)
- **Three White-Label Portals:** Customer, Reseller, and Admin (SaaS)
- **AI-Powered Intelligence:** Automated assistance for deployment, optimization, security, and support
- **100% Automation:** Provisioning, billing, renewals, suspensions, scaling
- **Enterprise Security:** OAuth 2FA, GST integration, audit logs, automated backups, monitoring
- **Modern Stack:** React 18 + MUI v6, Node.js/ASP.NET Core, microservices-ready, Docker/K8s

---

## Market Opportunity

### Target Market

1. **Primary:** Indian SMBs, agencies, freelancers needing Windows + Linux hosting
2. **Secondary:** Resellers (web agencies, freelancers) wanting white-label control panels
3. **Tertiary:** Enterprises needing hybrid Windows/Linux app hosting with self-service

### Market Size (India)

- Web hosting market: ₹8,500+ crore (2025)
- CAGR: 18.2% (2025-2030)
- Target: Capture 0.5% market share in Year 1 (₹42.5 crore revenue)

### Competitor Analysis

| Competitor | Strengths | Gaps (Our Opportunity) |
|------------|-----------|------------------------|
| **HestiaCP** | Free, lightweight, Linux-only | ❌ No Windows/ASP.NET<br>❌ Limited UI/UX<br>❌ No AI |
| **cPanel/WHM** | Industry standard, mature | ❌ Expensive (₹1,200+/month)<br>❌ Legacy UI<br>❌ No AI<br>❌ Manual workflows |
| **Plesk** | Windows + Linux support | ❌ Expensive<br>❌ Dated UX<br>❌ Limited automation |
| **Hostinger hPanel** | Modern UI, automation | ❌ Proprietary (not resellable)<br>❌ Limited customization |
| **Cloudways** | Managed cloud, good UX | ❌ No reseller panel<br>❌ No Windows<br>❌ Limited control |
| **DirectAdmin** | Lightweight, affordable | ❌ Basic UI<br>❌ Limited features |

### Key Differentiators

✅ **Only platform** offering Linux + Windows with modern, AI-driven UX  
✅ **White-label reseller portal** with full autonomy  
✅ **100% API-driven automation** (no SSH/RDP required)  
✅ **Built-in AI assistant** for support, security, and optimization  
✅ **Native billing + GST** (no WHMCS dependency)  
✅ **Modern React 18 + MUI v6** interface (vs. jQuery/Bootstrap 3)  

---

## Revenue Model

### Pricing Strategy

| Tier | Target | Price (INR/month) | Features |
|------|--------|-------------------|----------|
| **Starter** | Individual developers | ₹499 | 1 server, 10 sites, 50GB storage |
| **Professional** | Small agencies | ₹1,499 | 3 servers, 50 sites, 200GB storage |
| **Business** | Growing agencies | ₹2,999 | 10 servers, 200 sites, 1TB storage |
| **Reseller Basic** | Freelance resellers | ₹4,999 | White-label, 50 customers |
| **Reseller Pro** | Agency resellers | ₹9,999 | White-label, 200 customers, API |
| **Enterprise** | Large resellers | ₹19,999 | Unlimited, dedicated support |

### Revenue Streams

1. **SaaS Subscriptions:** 70% of revenue
2. **Usage-Based (storage, bandwidth, compute):** 15%
3. **Premium AI Features:** 10%
4. **Professional Services (migration, support):** 5%

### Financial Projections (Year 1)

- **Month 1-3:** Beta (50 users, ₹0 revenue)
- **Month 4-6:** Launch (500 users, ₹5 lakh/month)
- **Month 7-9:** Growth (2,000 users, ₹18 lakh/month)
- **Month 10-12:** Scale (5,000 users, ₹42 lakh/month)
- **Year 1 Total:** ₹2.1 crore revenue

---

## Success Metrics (KPIs)

### North Star Metric
**Active Hosted Websites:** Number of live websites on the platform

### Product KPIs

| Metric | Target (Month 6) | Target (Month 12) |
|--------|------------------|-------------------|
| Active Users | 500 | 5,000 |
| Active Websites | 2,000 | 25,000 |
| Resellers | 20 | 150 |
| Monthly Recurring Revenue (MRR) | ₹5 lakh | ₹42 lakh |
| Churn Rate | <5% | <3% |
| Customer Acquisition Cost (CAC) | ₹1,500 | ₹1,000 |
| Lifetime Value (LTV) | ₹18,000 | ₹25,000 |
| Net Promoter Score (NPS) | 40+ | 60+ |
| Uptime SLA | 99.9% | 99.95% |

### Technical KPIs

| Metric | Target |
|--------|--------|
| API Response Time (p95) | <200ms |
| Provisioning Time (new site) | <60 seconds |
| Dashboard Load Time | <1.5 seconds |
| Test Coverage | >80% |
| Security Scan (Critical CVEs) | 0 |
| Deployment Frequency | Daily |
| Mean Time to Recovery (MTTR) | <30 minutes |

---

## Product Principles

1. **Automation First:** Every manual task must have an API and UI automation path
2. **AI-Augmented:** AI assists, but humans control (no black-box decisions)
3. **Security by Default:** Secure by default, compliance-ready from day one
4. **Developer-Friendly:** RESTful APIs, webhooks, CLI, SDKs
5. **White-Label Ready:** Every reseller gets their own brand experience
6. **Observable:** Real-time monitoring, logging, alerting for all components
7. **Modern Stack Only:** No legacy dependencies (latest stable versions only)
8. **Production-Ready:** No mocks, stubs, placeholders, or test/dev code in production

---

## Repository Structure

```
webhost/
├── .github/
│   ├── workflows/           # GitHub Actions CI/CD
│   ├── ISSUE_TEMPLATE/
│   └── PULL_REQUEST_TEMPLATE.md
├── docs/                    # All project documentation
│   ├── PROJECT_OVERVIEW.md  # This file
│   ├── ARCHITECTURE.md
│   ├── ROADMAP.md
│   ├── TECH_STACK.md
│   ├── FEATURES.md
│   ├── SECURITY.md
│   ├── COPILOT_INSTRUCTIONS.md
│   ├── API_SPECIFICATION.md
│   └── adr/                 # Architecture Decision Records
├── apps/
│   ├── admin-portal/        # React + MUI (Admin SaaS panel)
│   ├── reseller-portal/     # React + MUI (Reseller panel)
│   ├── customer-portal/     # React + MUI (Customer panel)
│   ├── api-gateway/         # Node.js API Gateway
│   ├── auth-service/        # OAuth 2.0 + 2FA service
│   ├── billing-service/     # Billing, subscriptions, GST
│   ├── provisioning-service/# Linux + Windows provisioning
│   ├── ai-assistant-service/# GPT-4 AI features
│   └── notification-service/# Email, SMS, webhooks
├── packages/
│   ├── ui-components/       # Shared MUI components
│   ├── utils/               # Shared utilities
│   └── types/               # Shared TypeScript types
├── infra/
│   ├── terraform/           # IaC (Terraform)
│   ├── ansible/             # Configuration management
│   ├── k8s/                 # Kubernetes manifests
│   └── docker/              # Dockerfiles
├── scripts/
│   ├── setup-dev.sh
│   ├── migrate-db.sh
│   └── backup.sh
├── tests/
│   ├── e2e/                 # Playwright E2E tests
│   ├── integration/
│   └── performance/
├── .copilot/                # GitHub Copilot instructions
├── package.json             # Monorepo root
├── turbo.json               # Turborepo config
├── README.md
└── LICENSE
```

---

## Next Steps

1. ✅ Review & Approve this overview document
2. 📝 Review detailed documentation files (being created now)
3. 🚀 Set up repository and initial project structure
4. 💻 Begin Phase 1 (Foundation & MVP)

---

## Document History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-11-12 | @techfixind | Initial project overview |

---

**Confidential:** This document contains proprietary information of techfixind.