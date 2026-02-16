# Copilot Context & Instructions

## Project Overview

**Monto** is a learning platform for students and teachers.

- **Core Functionality**: Video sharing, organization (Class/Course/Chapter), and consumption.
- **Unique Selling Point**: AI-driven features (Transcription + Q&A Chatbot).

## Tech Stack

### Backend

- **Framework**: Laravel (PHP 8.2+)
- **API**: API Platform (integrated with Laravel)
- **Database**: MySQL 8.0 or PostgreSQL (Performance focus)
- **Queue/Cache**: Redis (Planned)
- **Video Processing**: FFmpeg (for WebM conversion/compression)
- **Deployment**: Ansible

### Frontend

- **Web**: React, TypeScript, Vite, Tailwind CSS, Shadcn UI
- **Mobile**: (Planned)

### AI Architecture

- **Transcription**: On-demand (Whisper or similar)
- **LLM**: External API initially, moving to self-hosted later.
- **RAG**: Answering questions based on video transcriptions.

## Architectural Decisions

- **Authentication**: Laravel Passport/Sanctum implementing OAuth. Frontend uses **HttpOnly Cookies** for security (HTML5 Storage avoided).
- **Video Storage**: Local filesystem with Docker volume persistence.
- **Video Processing**: Videos are processed via FFmpeg upon upload to ensure web compatibility (WebM) and size limits (~10 mins).
- **API Design**: Hybrid approach using Laravel Controllers and API Platform resources.

## Conventions

- **Code Style**: PSR-12 for PHP, Prettier/ESLint for TypeScript.
- **Docker**: All services containerized (App, Web Server, DB, Redis, etc.).
- **Environment**: Linux.
