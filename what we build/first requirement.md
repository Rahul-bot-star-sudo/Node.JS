## First Requirement

I want two users to be able to join a chat and communicate with each other.

But there is a problem:

**How will the system know which user sent a particular message?**

To solve this problem, I need to create an **authentication system**.

I will:

1. Allow users to register using their phone number.
2. Generate an OTP.
3. Verify the OTP.
4. After successful verification, redirect the user directly to their profile.

Now I need to start building the system.

For that, I will need:

- A **database** to store user information.
- A **backend** to handle the application logic.
- A **frontend** for the user interface.
- **APIs** to allow the frontend and backend to communicate with each other.

So my initial system will look like:

**User → Frontend → API → Backend → Database**

After authentication is completed, I can move toward the actual **chat functionality**.

---
