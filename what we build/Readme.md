
# Your exact learning loop

For **every small task**, I recommend we follow this:

```text
┌─────────────────────────┐
│ 1. TASK                  │
│ What are we building?   │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 2. WHY                   │
│ Why does the app need it?│
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 3. CONCEPTS              │
│ Level 1                  │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 4. RELATED CONCEPTS      │
│ Level 2                  │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 5. UNDERSTAND            │
│ Learn only what's needed │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 6. BUILD                 │
│ You write the code       │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 7. TEST                  │
│ Break it / observe it    │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 8. RECALL                │
│ Rebuild without notes    │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 9. EXPLAIN               │
│ Explain flow verbally    │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 10. INTERVIEW            │
│ Level 3 questions        │
└────────────┬────────────┘
             ↓
┌─────────────────────────┐
│ 11. NEXT TASK            │
└─────────────────────────┘
```

## One more thing I strongly recommend

Maintain **three separate things** while we build your chat application:

### ① Project notes

```text
What we implemented
```

### ② Concept notes

```text
What I learned
```

### ③ Recall questions

```text
Can I answer this without looking?
```

For example:

```text
EXPRESS
───────
Concept:
Express is a Node.js web framework.

Recall:
1. What is Express?
2. Why do we use it?
3. What is app?
4. What does app.get() do?
5. What is req?
6. What is res?
7. What does app.listen() do?
8. What is a port?
9. What happens when GET / arrives?
10. Node.js vs Express?
```
