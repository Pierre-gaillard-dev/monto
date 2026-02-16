# Monto
Monto is a Learning platform for students and teachers. Students can access videos provided by their teachers. Teachers can add ressources using youtube video's url or by uploading their own videos.

## Technologies

### Back-end (API)
- **Framework**: Laravel (PHP 8.5) with API Platform
- **Deployment**: Ansible
- **Database**: MySQL or PostgreSQL (TBD - focus on performance)
- **Cache**: Redis (TBD)
- **Video Processing**: FFmpeg (conversion to WebM, compression)

### Web Front-end
- React
- Typescript
- Vite
- Tailwind CSS
- Shadcn UI
- **Auth Strategy**: HttpOnly Cookies (Secure)

### Mobile Front-end
(to be added)

## Features

### Authentication & Users
- **OAuth** based authentication (Laravel)
- **Roles**: Admin, Teacher, Student
- **Registration**: Invitation only system

### Content Management
- **Organization**: Hierarchical structure: Class > Course > Chapter
- **Flexibility**: Videos/Resources can appear in multiple locations
- **Visibility**: Draft/Private mode for courses, chapters, or individual videos
- **Video Storage**: Local storage
- **Limits**: Video duration limit approx. 10 mins

### AI & Learning
- **Transcription**: On-demand video transcription (used as knowledge source)
- **Q&A Agent**: AI assistant answering questions based on video content (RAG approach)
- **Architecture**: LLM via external API initially, self-hosted planned
- **Analytics**: Teachers can view student activity and statistics

## Installation
(to be added)
