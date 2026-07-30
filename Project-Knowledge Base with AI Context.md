Berikut adalah versi **final yang saya rekomendasikan** untuk **Project Knowledge Base with AI Context**. Struktur ini sudah disederhanakan, berorientasi AI Agent, scalable untuk project kecil hingga enterprise, dan menghindari dokumentasi yang terlalu kompleks.

---

# Project-Knowledge Base with AI Context.md

# PROJECT KNOWLEDGE BASE WITH AI CONTEXT

## Purpose

Buat sistem dokumentasi project yang:

* Menjadi Single Source of Truth (SSOT)
* Menjadi Knowledge Base Project
* Menjadi AI Context Repository
* Menjadi Audit Trail seluruh aktivitas AI Agent
* Mendukung onboarding developer baru
* Mendukung maintenance jangka panjang
* Mendukung multi-agent workflow
* Mendukung pengembangan sistem yang scalable

Dokumentasi harus mudah dipahami manusia maupun AI Agent.

---

# DIRECTORY STRUCTURE

```text
context/
│
├── PRD.md
├── PROJECT_STATE.md
├── README.md
│
├── 01-project/
│   ├── overview.md
│   ├── architecture.md
│   ├── database.md
│   └── tech-stack.md
│
├── 02-development/
│   ├── conventions.md
│   ├── api.md
│   ├── testing.md
│   └── deployment.md
│
├── 03-management/
│   ├── progress.md
│   ├── backlog.md
│   ├── decisions.md
│   └── changelog.md
│
├── 04-agent-output/
│   ├── README.md
│   ├── backend/
│   ├── frontend/
│   ├── database/
│   ├── devops/
│   ├── documentation/
│   └── research/
│
└── 05-modules/
    ├── auth.md
    ├── dashboard.md
    ├── user-management.md
    ├── reporting.md
    ├── verification.md
    ├── execution.md
    ├── notification.md
    ├── audit-trail.md
    └── settings.md
```

---

# DOCUMENT PRIORITY

Semua AI Agent wajib membaca dokumen dengan urutan berikut:

```text
1. PRD.md
2. PROJECT_STATE.md
3. 03-management/decisions.md
4. File modul terkait
5. Dokumen pendukung lainnya
```

Contoh:

Jika mengerjakan modul Notification:

```text
PRD.md
PROJECT_STATE.md
03-management/decisions.md
05-modules/notification.md
```

---

# ROOT FILES

## PRD.md

Dokumen utama project.

Seluruh requirement bisnis dan sistem harus berasal dari file ini.

### Template

```md
# Project Overview

## Project Name

## Description

## Problem Statement

## Objectives

---

# Business Goals

## KPI

## Success Metrics

---

# Stakeholders

## Roles

## Responsibilities

---

# Functional Requirements

## Modules

- Authentication
- Dashboard
- Reporting
- Notification

---

# Non Functional Requirements

## Security

## Scalability

## Performance

## Availability

---

# Scope

## In Scope

## Out Scope

---

# Acceptance Criteria
```

---

## PROJECT_STATE.md

Dokumen yang selalu diperbarui setelah sesi kerja.

### Template

```md
# Current Project State

## Current Sprint

## Current Task

## Last Completed Task

## Current Module

## Known Issues

## Blockers

## Next Recommended Action

## Related Modules

## Last Updated
```

---

## README.md

Ringkasan project.

### Template

```md
# Project Name

## Overview

## Goals

## Architecture Summary

## Tech Stack

## Folder Structure

## Workflow

1. Read PRD
2. Read Project State
3. Read Module Context
4. Implement Task
5. Update Documentation
```

---

# 01-PROJECT

Folder informasi global project.

---

## overview.md

Berisi:

* Ringkasan sistem
* Stakeholder
* Scope
* Tujuan project

---

## architecture.md

Berisi:

```md
# High Level Architecture

# Components

# Services

# Modules

# Data Flow

# Infrastructure

# Security Layer

# External Integrations
```

---

## database.md

Berisi:

```md
# Database Overview

# ERD

# Main Tables

# Relationships

# Naming Conventions

# Migration Strategy
```

Catatan:

Detail tabel setiap modul disimpan pada file modul masing-masing.

---

## tech-stack.md

Berisi:

```md
# Frontend

# Backend

# Database

# Infrastructure

# DevOps

# Monitoring

# Third Party Services
```

---

# 02-DEVELOPMENT

---

## conventions.md

Berisi:

```md
# Naming Convention

# Folder Structure

# Coding Standards

# Git Standards

# Documentation Standards
```

---

## api.md

Berisi standar API global.

```md
# Authentication Standard

# Response Format

# Error Format

# Pagination Standard

# Validation Standard
```

---

## testing.md

Berisi:

```md
# Unit Test

# Integration Test

# E2E Test

# UAT

# Regression Testing
```

---

## deployment.md

Berisi:

```md
# Environment

# Docker

# CI/CD

# VPS

# Monitoring

# Backup Strategy

# Disaster Recovery
```

---

# 03-MANAGEMENT

---

## progress.md

```md
# Progress

Overall: 0%

## Completed

## In Progress

## Blocked

## Next Steps
```

---

## backlog.md

```md
| ID | Priority | Status | Module | Task |
|------|----------|----------|----------|----------|
```

---

## decisions.md

```md
## D001

Date:

Context:

Decision:

Alternatives:

Impact:

Status:
```

---

## changelog.md

```md
## YYYY-MM-DD HH:MM

### Added

### Changed

### Fixed

### Removed

### Security
```

---

# 04-AGENT-OUTPUT

Menyimpan seluruh hasil kerja AI Agent.

---

## Struktur

```text
backend/
└── YYYY/
    └── MM/
        └── DD/
            └── task-name.md
```

---

## Template Output AI Agent

```md
# Metadata

Date:

Agent:

Model:

Task:

Module:

Status:

---

# Objective

---

# Input Context

---

# Analysis

---

# Solution

---

# Generated Artifacts

---

# Decisions

---

# Risks

---

# Follow Up Tasks

---

# References
```

---

# 05-MODULES

## Filosofi

Satu file markdown untuk satu modul.

Tidak menggunakan subfolder.

Tujuannya:

* Mudah dicari AI Agent
* Mudah dibaca developer
* Mengurangi fragmentasi dokumentasi
* Mengurangi perpindahan file

---

# TEMPLATE MODUL

Contoh:

`reporting.md`

```md
# MODULE: REPORTING

## Overview

Deskripsi modul.

---

## Objectives

Tujuan modul.

---

## Stakeholders

### User

### Admin

### Manager

---

## Functional Requirements

### FR-001

### FR-002

### FR-003

---

## Business Rules

### BR-001

### BR-002

---

## Workflow

### Create

### Review

### Approve

### Reject

---

## Database Design

### Tables

### Columns

### Relationships

### Constraints

### Indexes

---

## Backend Design

### Services

### Repositories

### Actions

### Jobs

### Events

### Policies

---

## API Endpoints

### GET

### POST

### PUT

### DELETE

---

## Frontend Design

### Pages

### Components

### State Management

### Navigation

---

## UI / UX Requirements

### Layout

### Responsive Behavior

### Accessibility

---

## Validation Rules

---

## Security Rules

---

## Testing Scenarios

### Unit Test

### Integration Test

### UAT

---

## Dependencies

### Internal Modules

### External Services

---

## AI Agent Instructions

### Backend Agent

### Frontend Agent

### Database Agent

### QA Agent

### DevOps Agent

---

## Known Issues

---

## Future Improvements
```

---

# AI AGENT GOVERNANCE

Sebelum mengerjakan task:

Wajib membaca:

```text
PRD.md
PROJECT_STATE.md
03-management/decisions.md
05-modules/[module].md
```

---

Jika menghasilkan perubahan sistem:

Wajib memperbarui:

```text
03-management/changelog.md
03-management/progress.md
03-management/backlog.md
```

---

Jika menghasilkan keputusan baru:

Wajib memperbarui:

```text
03-management/decisions.md
```

---

Jika menghasilkan output:

Wajib menyimpan ke:

```text
04-agent-output/
```

---

# EXPECTED OUTPUT

Ketika struktur ini digunakan pada project baru, AI Agent harus mampu:

1. Memahami tujuan project.
2. Memahami kondisi project saat ini.
3. Memahami modul yang sedang dikerjakan.
4. Memahami database terkait modul.
5. Memahami backend logic.
6. Memahami frontend dan UI.
7. Memahami keputusan yang telah dibuat.
8. Menyimpan seluruh hasil kerjanya.
9. Memperbarui dokumentasi secara otomatis.
10. Menjaga seluruh knowledge project tetap konsisten selama siklus hidup project.

---

**Kesimpulan:** Ini adalah versi yang paling seimbang antara **kesederhanaan**, **kemudahan maintenance**, **efektivitas context untuk AI Agent**, dan **skalabilitas untuk project yang berkembang besar** tanpa membuat struktur folder menjadi terlalu rumit.
