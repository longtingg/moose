# EduPulse One

A lightweight, adaptive **web-based school management system** designed for low-end and high-end devices, including phones with **1GB RAM**.

## Vision
EduPulse One helps schools, teachers, parents, and students manage academic records in one secure platform with:
- Fast, low-memory UI
- Multi-role access control
- Cross-browser compatibility
- Result publishing and performance tracking

## Core User Roles
1. **School Administration**
   - Full access to students, teachers, classes, reports, and analytics.
   - Print/export report forms and term summaries.
2. **Teacher**
   - Access only assigned classes/subjects.
   - Enter and edit scores and remarks.
   - View students tied to their teaching load.
3. **Parent/Student Portal**
   - Login using a unique ID + password.
   - Account linked to parent email/phone.
   - View results and student progress.
   - Receive student results by SMS and/or email.
4. **Developer Support Role**
   - Restricted troubleshooting access.
   - Default credentials can exist only in development mode and must be rotated/disabled in production.

## Product Requirements (MVP)
- Secure authentication for Admin, Teacher, Parent/Student, Developer Support.
- Role-based authorization.
- Student profiles linked to parent contact details.
- Score entry + editing by authorized teachers.
- Result computation and printable report forms for administration.
- Activity logs for sensitive operations.
- Automated result delivery to parent contacts via SMS and/or email.

## UI/UX and Performance Targets
- Mobile-first responsive layout.
- Works smoothly on 1GB RAM phones using:
  - small bundles
  - code splitting
  - low-JS pages where possible
  - image optimization and lazy loading
- Browser support targets:
  - Chrome (latest 2)
  - Edge (latest 2)
  - Firefox (latest 2)
  - Safari (latest 2)
  - Android WebView (modern baseline)

## Suggested Technical Stack
- **Frontend:** React + Vite + Tailwind CSS (or lightweight component primitives)
- **Backend:** Node.js (Fastify or Express)
- **Database:** PostgreSQL
- **Cache/Queue (optional):** Redis
- **Auth:** JWT with refresh tokens + optional OTP for parent login recovery
- **Deployment:** Docker + Nginx

## Security Notes
- Store passwords with Argon2 or bcrypt.
- Enforce HTTPS and secure cookies.
- Add rate limiting and login lockout.
- Developer support account must be disabled in production by default.

## Suggested Initial Data Model
- `schools`
- `admins`
- `teachers`
- `students`
- `parents`
- `classes`
- `subjects`
- `teacher_assignments`
- `results`
- `attendance`
- `notifications`
- `notification_logs`
- `audit_logs`

## Next Build Milestones
1. Set up monorepo structure (`apps/web`, `apps/api`, `packages/shared`).
2. Implement authentication + role guards.
3. Build dashboards per role.
4. Add score entry and report generation.
5. Add SMS/email result notification service for parents.
6. Add audit logs and system health dashboard.

## Project Status
✅ Project initiated with baseline requirements and architecture direction.
