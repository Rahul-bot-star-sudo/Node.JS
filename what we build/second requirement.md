### Create User Without DB — CLI

**Start application**

---

### 1. Think where input comes from

```text
Give user one message to enter their name.
```

**JS/Node concept needed:**

```text
Node.js readline module
```

Because we need to **take input from the terminal**.

---

### 2. What happens when user gives input?

```text
Store the name in memory and use it.
```

**JS concept needed:**

```text
Variable
```

For example, conceptually:

```js
let name;
```

The user's input gets assigned to `name`.

---

### 3. What response do we give to the user?

```text
Show the user their name.
```

**JS concept needed:**

```text
console.log()
```

Because we need to **display output in the terminal**.

---

So your final thinking becomes:

```text
Requirement
    ↓
Create user without DB using CLI
    ↓
1. INPUT
   User enters name
   → readline

    ↓
2. PROCESS / MEMORY
   Store name
   → variable

    ↓
3. OUTPUT
   Show name
   → console.log()
```
