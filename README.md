# 🛡️ RBAC - Role-Based Access Control
# Am I Authorised

**Am I Authorised** is a **role-based access control (RBAC)** application that demonstrates fine-grained permission management in a modern web application. The system enforces **backend-driven authorization**, so pages, menus, buttons, and options are enabled or disabled based on the logged-in user’s role and permissions. The frontend is intentionally “dumb” — all control logic is enforced by the backend via JWT claims.

---

## 🧰 Tech Stack

- **Backend:** ASP.NET Core (.NET 8)   
- **Frontend:** Angular 21   
- **Database:** PostgreSQL   
- **Styling:** Bootstrap & Angular Material   

---

## 🏗️ System Overview

- Users are assigned **roles**: Admin , Employee , Manager , Auditor   
- Each role has **specific permissions**  
- All access control logic is handled by the backend   
- Frontend UI reacts dynamically based on the backend’s validation   
- JWT tokens carry both the user’s role and associated permissions   

## 📂 Repositories

This project is organized as multiple repositories to ensure clear separation of concerns.

| Component | Description | Repository |
|----------|------------|------------|
| Backend API | Authentication, REST APIs, persistence logic | 🔗 [Backend Repository](https://github.com/Balasubramanya777/am-i-authorised-.net) |
| Frontend | Angular application with collaborative editor | 🔗 [Frontend Repository](https://github.com/Balasubramanya777/am-i-authorised-angular) |


### 👥 Roles and Permissions

- **Admin :** Can create new users  
- **Auditor :** Can view roles and users  
- **Employee :** Can create, save, and submit applications  
- **Manager :** Can approve or reject applications, but cannot create or edit  

All permissions are included in the JWT, so backend APIs validate every request before processing it. This ensures that security is enforced at the backend, while the frontend dynamically enables or disables UI elements based on user permissions.

---

## 🖥️ Frontend Behavior

- Pages, menus, buttons, and actions are **enabled or disabled dynamically** based on the JWT claims from the backend  
- Frontend contains **no sensitive logic** for authorization  
- Angular Material and Bootstrap are used for styling and responsive layout   

---

## 🔄 Application Flow

1. User logs in → backend authenticates and issues JWT with role and permissions 
2. JWT is sent with each request → backend validates claims
3. Frontend renders pages, menus, and buttons according to the permissions received
4. Actions are allowed or denied based on backend validation

---

## 🔐 Security Considerations

- All authorization decisions are **enforced by the backend**  
- JWT includes both **role** and **permission claims**   
- No sensitive logic is implemented on the frontend  
- Policies are declarative and easily extendable for future roles and permissions   

---

## ✨ Features

- Role-based access control with fine-grained permissions   
- Backend-driven authorization with JWT   
- Angular 21 frontend with Bootstrap & Angular Material 
- PostgreSQL database for user, role, and application data 
- Extensible for new roles and permissions 
