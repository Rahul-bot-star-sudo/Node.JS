Now don't jump directly to code. Use this process:

> **Requirement → Break into smaller problems → Find concepts → Design flow → Algorithm → Code → Test → Debug**

## Requirement

> **Create users without any DB using CLI.**

### Step 1 — Break the requirement into problems

Ask:

```text
What does "create user" actually mean?
```

We need:

```text
1. Start Node.js application
2. Ask user for their name
3. Receive the name
4. Store the name in memory
5. Give the user an ID
6. Show the created user
```

---

## Step 2 — Ask: "How can JavaScript do each thing?"

Now you discover the concepts:

| Problem | Concept |
|---|---|
| Run JS outside browser | Node.js |
| Get input from terminal | `readline` |
| Store user's name | Variable |
| Represent a user | Object |
| Store multiple users | Array |
| Generate ID | Variable/counter |
| Show result | `console.log()` |

Notice what happened.

You **didn't memorize a tutorial** saying:

> "For user creation, use readline + array + object."

Instead, you looked at the requirement and asked:

> **"What does my program need to do, and what JS concept can perform that job?"**

That's the skill you're trying to develop.

---

## Step 3 — Design the data

Before coding, decide what one user looks like.

```text
User
├── id
└── name
```

For example:

```js
{
  id: 1,
  name: "Rahul"
}
```

And because there can be multiple users:

```js
users = [
  {
    id: 1,
    name: "Rahul"
  },
  {
    id: 2,
    name: "Amit"
  }
]
```

That's your **in-memory database**, although technically it's just an array in application memory.

---

## Step 4 — Design the flow

Now draw the execution:

```text
START
  ↓
Create empty users array
  ↓
Ask: "Enter your name:"
  ↓
User enters name
  ↓
Generate ID
  ↓
Create User object
  ↓
Push user into users array
  ↓
Display user
  ↓
END
```

---

## Step 5 — Write the algorithm

In plain English first:

```text
1. Start the application.
2. Create an empty array called users.
3. Ask the user for their name.
4. Receive the name.
5. Generate a unique ID.
6. Create a user object using ID and name.
7. Store the object in users.
8. Display the created user.
```

**Only now should you write code.**

---

## And this is how you learn when you don't know the concepts

Suppose you reach:

> "How do I get input from CLI?"

You don't know.

That's okay.

Now your question becomes specific:

> **"How does Node.js receive input from the terminal?"**

You learn **readline**.

Then:

> "How do I store multiple users?"

You learn **arrays**.

Then:

> "How do I represent one user?"

You learn **objects**.

This is much better than trying to learn all of JavaScript first.

### Your learning loop

```text
Requirement
     ↓
I don't know how
     ↓
Identify the specific unknown
     ↓
Learn that concept
     ↓
Use it
     ↓
Run program
     ↓
Error?
     ↓
Debug
     ↓
Understand
     ↓
Next requirement
```

This is how you can learn the project **while actually building it**.

And for your live-chat project, this is the path I'd recommend: **we take one requirement at a time, and you discover the concepts needed for that requirement before writing the implementation.**