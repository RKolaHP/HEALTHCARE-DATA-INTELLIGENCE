# Healthcare Data Intelligence Platform

> **Portfolio-safe reconstruction of a production-style healthcare data engineering platform**

**Data Engineering × Microsoft Fabric × OneLake × Lakehouse × PySpark × SQL × Delta Lake × Data Quality**

---

## Overview

This project demonstrates a healthcare-oriented data engineering architecture designed to transform raw operational data into validated analytical datasets.

The implementation is intentionally portfolio-safe.

It does **not** contain:

- Patient information
- Protected health information
- Employer source code
- Internal URLs
- Proprietary schemas
- Credentials
- Confidential business rules
- Restricted datasets

The demonstration uses synthetic data.

---

# Architecture

```text
                   SYNTHETIC SOURCE DATA
                            │
                            ▼
                    ┌───────────────┐
                    │    BRONZE     │
                    │ Raw / Source  │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │    QUALITY    │
                    │     GATE      │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │    SILVER     │
                    │ Clean / Valid │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │    QUALITY    │
                    │     GATE      │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │     GOLD      │
                    │ Curated / KPI │
                    └───────┬───────┘
                            │
                  ┌─────────┴─────────┐
                  ▼                   ▼
              BI / KPIs         ML / Analytics
