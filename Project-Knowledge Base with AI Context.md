# Project Knowledge Base with AI Context

# PROJECT KNOWLEDGE BASE WITH AI CONTEXT

## Purpose

Buat sistem dokumentasi project yang:

- Menjadi Single Source of Truth (SSOT)
- Menjadi Knowledge Base Project
- Menjadi AI Context Repository
- Menjadi Audit Trail seluruh aktivitas AI Agent
- Mendukung onboarding developer baru
- Mendukung maintenance jangka panjang
- Mendukung multi-agent workflow
- Mendukung pengembangan sistem yang scalable

Dokumentasi harus mudah dipahami manusia maupun AI Agent.

---

# DIRECTORY STRUCTURE

```text
context/
|-- PRD.md
|-- PROJECT_STATE.md
|-- README.md
|
|-- 01-project/
|   |-- overview.md
|   |-- architecture.md
|   |-- database.md
|   `-- tech-stack.md
|
|-- 02-development/
|   |-- conventions.md
|   |-- api.md
|   |-- testing.md
|   `-- deployment.md
|
|-- 03-management/
|   |-- progress.md
|   |-- backlog.md
|   |-- decisions.md
|   `-- changelog.md
|
|-- 04-agent-output/
|   |-- README.md
|   |-- backend/
|   |-- frontend/
|   |-- database/
|   |-- devops/
|   |-- documentation/
|   `-- research/
|
|-- 05-setup/
|   |-- local-development.md
|   |-- environment-variables.md
|   |-- database-setup.md
|   |-- docker-setup.md
|   `-- troubleshooting.md
|
`-- 06-modules/
    |-- auth.md
    |-- dashboard.md
    |-- user-management.md
    |-- reporting.md
    |-- verification.md
    |-- execution.md
    |-- notification.md
    |-- audit-trail.md
    `-- settings.md
```

---

# DOCUMENT PRIORITY

Semua AI Agent wajib membaca dokumen dengan urutan berikut:

```text
1. PRD.md
2. PROJECT_STATE.md
3. 05-setup/local-development.md (jika task perlu menjalankan project)
4. 03-management/decisions.md
5. File modul terkait
6. Dokumen pendukung lainnya
```

Contoh ketika mengerjakan modul Notification:

```text
PRD.md
PROJECT_STATE.md
05-setup/local-development.md
03-management/decisions.md
06-modules/notification.md
```

---

# ROOT FILES

## PRD.md

Dokumen utama project. Seluruh requirement bisnis dan sistem harus berasal dari file ini.

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
3. Read Setup Context
4. Read Module Context
5. Implement Task
6. Update Documentation
```

---

# 01-PROJECT

Folder informasi global project.

## overview.md

Berisi:

- Ringkasan sistem
- Stakeholder
- Scope
- Tujuan project

## architecture.md

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

## database.md

```md
# Database Overview

# ERD

# Main Tables

# Relationships

# Naming Conventions

# Migration Strategy
```

Detail tabel setiap modul disimpan pada file modul masing-masing.

## tech-stack.md

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

## conventions.md

```md
# Naming Convention

# Folder Structure

# Coding Standards

# Git Standards

# Documentation Standards
```

## api.md

Berisi standar API global.

```md
# Authentication Standard

# Response Format

# Error Format

# Pagination Standard

# Validation Standard
```

## testing.md

```md
# Unit Test

# Integration Test

# E2E Test

# UAT

# Regression Testing
```

## deployment.md

Dokumen deployment hanya membahas proses membawa aplikasi ke environment production atau staging.

```md
# Environment

# Build

# Docker Compose

# VPS or Cloud Server

# Nginx

# SSL

# CI/CD

# Monitoring

# Backup Strategy

# Disaster Recovery
```

---

# 03-MANAGEMENT

## progress.md

```md
# Progress

Overall: 0%

## Completed

## In Progress

## Blocked

## Next Steps
```

## backlog.md

```md
| ID | Priority | Status | Module | Task |
|----|----------|--------|--------|------|
```

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

## Struktur

```text
backend/
`-- YYYY/
    `-- MM/
        `-- DD/
            `-- task-name.md
```

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

# 05-SETUP

Folder ini mendokumentasikan cara menjalankan project dari nol di mesin lokal. Setup berbeda dari deployment dan tidak digabung ke `02-development/deployment.md`.

## Mengapa Setup Tidak Digabung ke deployment.md?

Setup berfokus pada:

```text
Install
  |
Configuration
  |
Database
  |
Dependencies
  |
Run Local
```

Contoh aktivitas setup:

- Install PHP, Node.js, Docker, dan PostgreSQL
- Clone repository
- Jalankan Composer install dan NPM install
- Generate application key
- Jalankan migration dan seeder
- Menjalankan aplikasi secara lokal

Deployment berfokus pada:

```text
Build
  |
Server
  |
CI/CD
  |
Production
  |
Monitoring
```

Contoh aktivitas deployment:

- VPS atau cloud server
- Docker Compose untuk production
- Nginx dan SSL
- CI/CD
- Backup dan monitoring

Pemisahan ini membuat developer baru dan AI Agent dapat memahami konfigurasi lokal tanpa mencampurnya dengan keputusan infrastructure production.

## Konteks Docker untuk Project

Jika repository memiliki `compose.yaml`, `compose.yml`, atau `docker-compose.yml`, Docker harus didokumentasikan sebagai bagian dari setup lokal. `05-setup/docker-setup.md` menjadi referensi utama untuk nama service, port, volume, network, dan perintah yang dijalankan di dalam container.

Dalam kondisi tersebut, AI Agent dan developer wajib:

- Membaca `05-setup/docker-setup.md` sebelum menjalankan aplikasi atau service pendukung.
- Menggunakan nama service Compose untuk komunikasi antar-container, misalnya `DB_HOST=db`, bukan `localhost`.
- Menjalankan command aplikasi melalui `docker compose exec <app-service> ...` apabila runtime aplikasi berada di dalam container.
- Tidak menjalankan `docker compose down -v` tanpa memastikan data volume lokal memang boleh dihapus.

Dokumentasi Docker harus menyebutkan file konfigurasi yang digunakan, service yang tersedia, URL lokal, port host, serta variable environment khusus container. Jika Docker tidak digunakan, `docker-setup.md` harus menyatakan status tersebut dan menunjuk ke alur setup non-Docker.

## local-development.md

Dokumen paling penting untuk menjalankan aplikasi di lokal.

### Template

````md
# Local Development Setup

## Prerequisites

- PHP 8.4
- Node 22
- PostgreSQL 17
- Docker
- Git

---

## Docker Runtime (Jika Digunakan)

Jika project menggunakan Docker, jalankan service melalui Compose dan gunakan perintah di `docker-setup.md`. Ganti `<app-service>` dengan nama service aplikasi yang sebenarnya.

```sh
docker compose up -d --build
docker compose exec <app-service> php artisan key:generate
docker compose exec <app-service> php artisan migrate --seed
```

---

## Clone Repository

```sh
git clone ...
```

---

## Install Dependencies

```sh
composer install
npm install
```

---

## Environment Setup

```sh
cp .env.example .env
```

---

## Generate Key

```sh
php artisan key:generate
```

---

## Database Setup

```sh
php artisan migrate
php artisan db:seed
```

---

## Build Assets

```sh
npm run build
```

---

## Run Application

```sh
php artisan serve
npm run dev
```

---

## Verification

- Login page muncul
- Database terkoneksi
- Migration sukses
````

## environment-variables.md

Dokumentasi seluruh environment variable. Dokumen ini membantu AI Agent memahami konfigurasi sistem tanpa perlu menebak nilai atau kegunaan setiap variable.

### Template

```md
# Environment Variables

## APP

APP_NAME
APP_ENV
APP_DEBUG

---

## DATABASE

DB_CONNECTION
DB_HOST
DB_PORT

---

## REDIS

REDIS_HOST

---

## MAIL

MAIL_HOST

---

## STORAGE

AWS_ACCESS_KEY_ID

---

## DOCKER (Jika Digunakan)

COMPOSE_PROJECT_NAME
APP_PORT
DB_PORT
```

Setiap variable sebaiknya dilengkapi deskripsi, format nilai, default, dan keterangan apakah nilainya bersifat rahasia. Untuk Docker, jelaskan perbedaan antara port host dan port internal container. Jangan menyimpan secret aktual di dokumentasi.

## database-setup.md

Dokumen khusus untuk database lokal.

### Template

````md
# Database Setup

## PostgreSQL Version

17

---

## Docker Database Connection (Jika Digunakan)

Gunakan nama service database sebagai host, bukan `localhost`.

```text
DB_HOST=db
DB_PORT=5432
```

Port yang diekspos ke host hanya dipakai oleh tools yang berjalan di mesin lokal, seperti database client atau IDE.

---

## Create Database

```sql
CREATE DATABASE app_db;
```

---

## Migration

```sh
php artisan migrate
```

---

## Seeder

```sh
php artisan db:seed
```
````

## docker-setup.md

Dokumen ini digunakan jika project memakai Docker untuk development lokal. Catat konfigurasi aktual project; jangan mengasumsikan nama service, port, atau path volume.

### Template

````md
# Docker Setup

## Status

Docker digunakan untuk local development.

## Configuration Files

- compose.yaml
- Dockerfile
- .docker/ (jika ada)

## Prerequisites

- Docker Desktop atau Docker Engine
- Docker Compose v2

---

## Services

| Service | Purpose | Container Port | Host Port | Command Runtime |
|---------|---------|----------------|-----------|-----------------|
| app | Laravel application | 8000 | 8000 | Ya |
| db | PostgreSQL | 5432 | 5432 | Tidak |
| redis | Redis cache | 6379 | 6379 | Tidak |

Ganti tabel ini sesuai service yang benar-benar tersedia pada project.

---

## Environment Rules

- Gunakan nama service untuk koneksi antar-container, contoh: `DB_HOST=db`.
- Gunakan `localhost:<host-port>` hanya dari mesin host.
- Dokumentasikan semua variable Compose dan file environment yang digunakan.

---

## Build

```sh
docker compose build
```

---

## Run

```sh
docker compose up -d
```

---

## Status

```sh
docker compose ps
```

---

## Application Commands

Ganti `<app-service>` dengan service aplikasi yang sebenarnya.

```sh
docker compose exec <app-service> php artisan key:generate
docker compose exec <app-service> php artisan migrate --seed
docker compose exec <app-service> npm run dev
```

---

## Stop

```sh
docker compose down
```

---

## Logs

```sh
docker compose logs -f
```

---

## Reset Local Data

Perintah berikut menghapus volume beserta data lokal. Jalankan hanya jika data boleh dibuat ulang.

```sh
docker compose down -v
docker compose up -d --build
```
````

## troubleshooting.md

Dokumen masalah umum dan langkah penyelesaiannya. Ini mengurangi waktu onboarding dan membantu AI Agent melakukan diagnosis awal.

### Template

````md
# Common Issues

## Permission Denied

```sh
chmod -R 775 storage bootstrap/cache
```

---

## Vite Manifest Not Found

```sh
npm run build
```

---

## Database Connection Refused

Periksa:

DB_HOST
DB_PORT

---

## Docker Volume Error

```sh
docker compose down -v
docker compose up -d
```
````

---

# 06-MODULES

## Filosofi

Satu file markdown untuk satu modul. Tidak menggunakan subfolder.

Tujuannya:

- Mudah dicari AI Agent
- Mudah dibaca developer
- Mengurangi fragmentasi dokumentasi
- Mengurangi perpindahan file

# TEMPLATE MODUL

Contoh: `reporting.md`

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

Sebelum mengerjakan task, AI Agent wajib membaca:

```text
PRD.md
PROJECT_STATE.md
05-setup/local-development.md (jika task perlu menjalankan project)
03-management/decisions.md
06-modules/[module].md
```

Jika menghasilkan perubahan sistem, AI Agent wajib memperbarui:

```text
03-management/changelog.md
03-management/progress.md
03-management/backlog.md
```

Jika menghasilkan keputusan baru, AI Agent wajib memperbarui:

```text
03-management/decisions.md
```

Jika menghasilkan output, AI Agent wajib menyimpan ke:

```text
04-agent-output/
```

---

# EXPECTED OUTPUT

Ketika struktur ini digunakan pada project baru, AI Agent dan developer baru harus mampu:

1. Memahami tujuan dan kondisi project saat ini.
2. Menjalankan project dari nol di environment lokal.
3. Memahami konfigurasi environment dan database.
4. Memahami modul, database, backend logic, serta frontend terkait task.
5. Memahami keputusan yang telah dibuat.
6. Mengembangkan fitur dan mendokumentasikan hasil kerjanya.
7. Memperbarui knowledge project secara konsisten selama siklus hidup project.

**Kesimpulan:** Dengan `PRD.md`, `PROJECT_STATE.md`, `05-setup/`, `06-modules/`, dan `04-agent-output/`, project memiliki context yang cukup bagi AI Agent maupun developer baru untuk memahami, menjalankan, mengembangkan, dan mendokumentasikan sistem tanpa bergantung pada pembuat project.
