### Hum isme kya build karenge?

| Feature              | Real-world example          | System Design Concept      |
| -------------------- | --------------------------- | -------------------------- |
| User Registration    | Instagram, Amazon           | Authentication             |
| User Login           | Google, GitHub              | Authentication             |
| Password Security    | Almost every production app | Hashing                    |
| Access Token         | APIs                        | JWT / Token Authentication |
| Refresh Token        | Google, Amazon              | Token Lifecycle            |
| Logout               | Every secure application    | Session/Token invalidation |
| Roles                | GitHub, AWS                 | RBAC                       |
| Permissions          | AWS IAM, GitHub             | Authorization              |
| Protected APIs       | Banking/API systems         | Middleware                 |
| Admin APIs           | Admin panels                | Role-based authorization   |
| Account Lock/Disable | Banking, enterprise apps    | Security                   |
| Audit Logs           | AWS, enterprise systems     | Auditing                   |

---

# 🚀 Live Chat Application — Task Roadmap

## Phase 1 — CLI + JavaScript Fundamentals

**Goal:** Build a chat application that works completely in the terminal.

### Task 1 — Run JavaScript with Node.js

* Create `app.js`
* Print messages
* Run with `node app.js`
* Understand: JS → Node → Terminal

### Task 2 — Get user input

Build:

```text
====================
     LIVE CHAT
====================

Enter your name:
```

Learn:

* `process.stdin`
* input/output
* strings

### Task 3 — Create users

Represent users as objects:

```js
{
  id: 1,
  name: "Rahul"
}
```

Create multiple users.

Learn:

* objects
* arrays
* accessing data

### Task 4 — User menu

```text
1. View Users
2. Send Message
3. View Messages
4. Exit
```

Learn:

* conditions
* loops
* functions

### Task 5 — Send a message

```text
From: Rahul
To: Amit
Message: Hello
```

Create:

```js
{
  senderId: 1,
  receiverId: 2,
  text: "Hello"
}
```

### Task 6 — View conversation

```text
Rahul: Hello
Amit: Hi Rahul
Rahul: How are you?
```

Learn:

* arrays of objects
* filtering
* functions

### Task 7 — Organize the CLI project

Move from one file into:

```text
cli-chat/
├── app.js
├── users.js
├── messages.js
├── chat.js
└── utils.js
```

Learn:

**modules → imports → exports**

---

# Phase 2 — HTML + CSS

Now rebuild the **same application visually**.

### Task 8 — Create chat UI

Build:

```text
┌──────────────┬───────────────────────┐
│ Users        │ Amit                  │
│              ├───────────────────────┤
│ Rahul        │ Hello                 │
│ Amit         │              Hi       │
│ John         │                       │
│              ├───────────────────────┤
│              │ Message...     Send   │
└──────────────┴───────────────────────┘
```

Learn:

* HTML structure
* semantic elements

### Task 9 — Style the application

Learn:

* CSS
* Flexbox
* spacing
* colors
* responsive layout

### Task 10 — Make it responsive

Make it usable on:

```text
Desktop
Tablet
Mobile
```

---

# Phase 3 — Browser JavaScript

Now make the UI actually work.

### Task 11 — Send message from UI

```text
Type message
      ↓
Click Send
      ↓
Create message
      ↓
Display message
```

### Task 12 — User selection

Click:

```text
Amit
```

and open Amit's conversation.

### Task 13 — Conversation state

Maintain:

```text
Rahul ↔ Amit
Rahul ↔ John
Rahul ↔ Priya
```

Learn:

* state
* arrays
* objects
* DOM manipulation

### Task 14 — Search users

```text
Search: Am

→ Amit
```

### Task 15 — Message validation

Prevent:

```text
empty message
```

and show an error.

---

# Phase 4 — Convert UI into Components

Now introduce **React + TypeScript**.

Don't start React before this point.

### Task 16 — Create React project

Convert the existing UI into React.

### Task 17 — Create components

```text
ChatApp
├── Sidebar
│   ├── SearchUser
│   ├── UserList
│   └── UserItem
│
└── ChatWindow
    ├── ChatHeader
    ├── MessageList
    ├── Message
    └── MessageInput
```

### Task 18 — Props

Pass:

```text
User → UserItem
Message → Message
```

### Task 19 — State

Manage:

```text
selectedUser
messages
inputMessage
users
```

### Task 20 — Forms and events

Handle:

```text
typing
clicking
submitting
selecting users
```

---

# Phase 5 — Node.js Backend

Now we build the actual backend.

### Task 21 — Create Node.js + TypeScript project

```text
server/
├── src/
│   ├── app.ts
│   └── server.ts
└── package.json
```

### Task 22 — Create HTTP server

Understand:

```text
Request
   ↓
Server
   ↓
Response
```

### Task 23 — Add Express

Create:

```http
GET /api/health
```

Response:

```json
{
  "status": "ok"
}
```

### Task 24 — Users API

```http
GET /api/users
```

### Task 25 — Create user

```http
POST /api/users
```

### Task 26 — Messages API

```http
GET /api/messages/:userId
```

### Task 27 — Send message API

```http
POST /api/messages
```

---

# Phase 6 — Database

Now replace temporary arrays with a real database.

### Task 28 — Database setup

Use:

**PostgreSQL**

### Task 29 — Design database

Start with:

```text
users
messages
```

Relationship:

```text
User
 │
 ├── sends → Message
 │
 └── receives ← Message
```

### Task 30 — User CRUD

Implement:

```text
Create
Read
Update
Delete
```

### Task 31 — Message persistence

Send a message:

```text
Frontend
 ↓
API
 ↓
Service
 ↓
Database
```

Then reload the application.

The message should still exist.

---

# Phase 7 — Authentication

### Task 32 — Register

```http
POST /api/auth/register
```

### Task 33 — Login

```http
POST /api/auth/login
```

### Task 34 — Password hashing

Learn:

```text
Password
 ↓
bcrypt
 ↓
Hash
 ↓
Database
```

### Task 35 — JWT authentication

Learn:

```text
Login
 ↓
JWT
 ↓
Client
 ↓
Request
 ↓
Authorization
```

### Task 36 — Protected APIs

Only authenticated users can:

```text
View conversations
Send messages
View profile
```

---

# Phase 8 — Real-Time Chat

Now we make it **LIVE**.

### Task 37 — Understand WebSockets

First understand:

```text
HTTP:
Client → Request → Server → Response

WebSocket:
Client ←────────→ Server
```

### Task 38 — Add Socket.IO

Connect:

```text
React
 ↕
Socket.IO
 ↕
Node.js
```

### Task 39 — Real-time message

```text
Rahul sends message
       ↓
Server receives
       ↓
Server broadcasts
       ↓
Amit receives instantly
```

### Task 40 — Online/offline status

Show:

```text
🟢 Amit
⚪ John
```

### Task 41 — Typing indicator

```text
Amit is typing...
```

### Task 42 — Message delivery status

```text
✓ Sent
✓✓ Delivered
✓✓ Read
```

---

# Phase 9 — Production Features

### Task 43 — Error handling

Handle:

```text
400
401
403
404
500
```

### Task 44 — API validation

Validate:

```text
email
password
message
userId
```

### Task 45 — Security

Learn and implement:

```text
CORS
Helmet
Rate limiting
Input validation
Environment variables
Password hashing
JWT security
```

### Task 46 — Logging

Add structured backend logging.

### Task 47 — Testing

Test:

```text
Auth
Users
Messages
APIs
```

### Task 48 — Frontend error/loading states

Handle:

```text
Loading...
Sending...
Failed to send
No messages
User not found
```

---

# Phase 10 — Deployment

### Task 49 — Dockerize backend

### Task 50 — Production environment

Separate:

```text
Development
Production
```

### Task 51 — Deploy backend

### Task 52 — Deploy frontend

### Task 53 — Connect production database

### Task 54 — Final security check

### Task 55 — Final documentation

Create:

```text
README.md
ARCHITECTURE.md
API.md
DATABASE.md
```

---

# 🏁 Final Architecture

By the end, you'll have:

```text
                 LIVE CHAT
                     │
          ┌──────────┴──────────┐
          │                     │
       React                  Node.js
    TypeScript               TypeScript
          │                     │
          │ HTTP / WebSocket    │
          └──────────┬──────────┘
                     │
                  Services
                     │
                 PostgreSQL
```

And the learning progression is:

```text
CLI
 ↓
JavaScript
 ↓
HTML
 ↓
CSS
 ↓
Browser JS
 ↓
React + TypeScript
 ↓
Node.js
 ↓
Express
 ↓
REST API
 ↓
PostgreSQL
 ↓
Authentication
 ↓
WebSocket
 ↓
Testing
 ↓
Docker
 ↓
Deployment
```

### One important rule for us

**Don't try to complete all 55 tasks by reading tutorials.**

For every task, we'll use:

> **PROBLEM → QUESTIONS → LOGIC → FLOW → ALGORITHM → CODE → RUN → ERROR → DEBUG → UNDERSTAND**

So when you reach **Task 5**, for example, I won't simply give you the finished `sendMessage()` code. I'll first make you think:

> *“What information does a message need?”*
> *“Where should we store it?”*
> *“How do we know who sent it?”*
> *“How do we know who receives it?”*

That's how you'll actually learn programming while building the project.
