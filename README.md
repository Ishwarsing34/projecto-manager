# Project Management Application

A full-stack project management platform that allows teams to collaborate efficiently across multiple workspaces. Users can manage projects, assign tasks, invite members, track progress, and receive automated email notifications — all in one place.

---

## 🚀 Features

### 🏢 Workspaces
- Create and manage **multiple workspaces**
- Each workspace has its own members, projects, and tasks
- Workspace owners can invite members via email

### 👥 Member Management
- Invite users to workspaces using email invitations
- Role-based access (Admin / Member)
- Only authorized users can manage projects and tasks

### 📁 Projects
- Create and update projects inside a workspace
- Assign a **team lead** to each project
- Add workspace members to projects

### ✅ Tasks
- Create tasks with:
  - Priority (Low / Medium / High)
  - Status (Todo / In Progress / Done)
  - Due dates
- Assign tasks to members
- Update and delete tasks with proper permissions

### 📧 Email Notifications
- Automatic email sent when:
  - A user is invited to a workspace
  - A task is assigned to a member
- Reminder email sent if a task is **not completed by the due date**
- Emails handled asynchronously using background jobs

### 📊 Analytics Dashboard
- Visual analytics using charts
- Track project and task progress across workspaces

---

## 🛠️ Tech Stack

### Frontend
- **React**
- **Redux Toolkit**
- **Tailwind CSS**
- **Clerk** (Authentication & Organizations)
- **Charts / Analytics Libraries**

### Backend
- **Node.js**
- **Express.js**
- **PostgreSQL**
- **Prisma ORM**

### Background Jobs & Events
- **Inngest**
  - Handles email notifications
  - Scheduled task reminders
  - Event-driven workflows

### Deployment
- **Vercel** (Frontend & Serverless APIs)
- **PostgreSQL (Cloud-hosted)**

---

## 🧱 Architecture Overview

- **Clerk** handles authentication, users, and organizations
- **Backend API** manages business logic, permissions, and database operations
- **Prisma ORM** ensures type-safe database access
- **Inngest** listens to application events (task assigned, due date reached)
- **Nodemailer** sends transactional and reminder emails
- **Redux Toolkit** manages frontend state

---

## 📸 Application Preview

### Dashboard
_Add screenshot here_

<img width="1902" height="907" alt="image" src="https://github.com/user-attachments/assets/25a03ebd-7ad5-4e52-a6c3-36bc31e650f4" />

<img width="1876" height="891" alt="image" src="https://github.com/user-attachments/assets/1c64c1f5-3c8d-412e-bc47-cb32173e94b8" />



---

### Workspace View
_Add screenshot here_

<img width="358" height="398" alt="image" src="https://github.com/user-attachments/assets/1f466095-70ef-42f0-b9b7-4e0346d05a2a" />


---

### Project & Task Management
_Add screenshot here_

<img width="1877" height="907" alt="image" src="https://github.com/user-attachments/assets/d204e49d-5bf9-4d4a-9284-8beba2f47eba" />



---

### Analytics
_Add screenshot here_

<img width="1472" height="891" alt="image" src="https://github.com/user-attachments/assets/a0a6e20f-6a6b-4bd1-8153-f9074387b21e" />



<img width="1861" height="923" alt="image" src="https://github.com/user-attachments/assets/6ac2b2e5-15fc-46d7-9325-9482b9840ad2" />



<img width="1457" height="847" alt="image" src="https://github.com/user-attachments/assets/6c2eaddf-3a9d-4bcc-a125-e56852defde5" />



---

## 🔐 Authentication & Authorization

- Authentication handled by **Clerk**
- JWT-based secure API requests
- Role-based access control for:
  - Workspaces
  - Projects
  - Tasks

---

## 📬 Email & Notification Flow

1. Task assigned → Event triggered
2. Inngest background function executes
3. Email sent to assignee
4. If task is not completed by due date → Reminder email sent automatically

---

## 🧪 Local Setup

```bash
# Clone repository
git clone <your-repo-url>

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env

# Run development server
npm run dev
