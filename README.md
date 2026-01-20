# 🗂️ Kanban

**Real-Time Collaborative Task & Activity Dashboard (Next.js)**

Kanban is a **full-stack, real-time task management system** inspired by Trello, Linear, and Jira.  
Designed as a learning-heavy project to master:

- WebSockets
- Full-stack data flow
- Real-time synchronization
- State management
- Query optimization
- Scalable architecture

Built with the **PERN stack + Next.js (App Router)**.

---

## 🚀 Tech Stack

### Frontend
- **Next.js (App Router)** – Server & Client Components
- React 18
- Zustand / Redux Toolkit for state management
- Tailwind CSS
- WebSocket client

### Backend
- Node.js + Express
- WebSocket (ws / socket.io)
- Prisma ORM
- PostgreSQL

### Infrastructure
- PostgreSQL for persistence
- WebSockets for real-time sync
- REST APIs for mutations

---

## 🧠 Core Features

### 🧑‍🤝‍🧑 Workspaces & Teams
- Multiple workspaces
- Role-based membership (admin, member)

### 📋 Boards & Columns
- Boards inside workspaces
- Columns (lists) with ordered positions
- Drag & drop reordering

### 📝 Tasks
- Create, update, delete tasks
- Move tasks across columns
- Position-based ordering
- Due dates & status

### 💬 Comments
- Task-level threaded comments
- Real-time updates

### 🔔 Notifications
- Task assignments
- Mentions
- Unread tracking

### 📰 Activity Feed
- Append-only event log
- Board-level and task-level activity
- Optimized pagination

### ⚡ Real-Time Collaboration
- Live task creation
- Live task movement
- Live comments
- Selective broadcasting to connected users

---

## 🗄️ Data Model (High-Level)

**Main entities:**
- User
- Workspace
- WorkspaceMember
- Board
- Column
- Task
- TaskAssignment
- Comment
- Activity
- Notification

**Optimized with indexes for:**
- Column ordering
- Board activity feeds
- User notifications
- Real-time updates

---

## 🏗️ Project Structure

### Backend: `web-sockets-api/`
```bash
src/
  modules/
    auth/
    workspace/
    board/
    column/
    task/
    comment/
    activity/
    notification/
  websocket/
    index.ts
    handlers/
  prisma/
    schema.prisma
  lib/
    prisma.ts
    auth.ts
  routes.ts
  server.ts
