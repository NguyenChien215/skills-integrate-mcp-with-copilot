# Admin Mode Implementation

## Overview
This implements an authentication system for teachers to control student registrations.

## Features
- **Login System**: Teachers can log in using username and password
- **Protected Actions**: Only authenticated teachers can:
  - Register students for activities
  - Unregister students from activities
- **Public View**: Students and visitors can view activities and participants without logging in
- **Session Management**: Uses token-based authentication with browser localStorage

## Teacher Credentials

The default teacher accounts are stored in `src/teachers.json`:

- **Username**: admin  
  **Password**: password123

- **Username**: teacher1  
  **Password**: teach123

## How to Use

### For Teachers:
1. Click the "👤 Login" button in the top-right corner
2. Enter your username and password
3. Once logged in, you can:
   - Sign up students using the registration form
   - Remove students by clicking the ❌ button next to their name

### For Students:
- View all available activities and see who is registered
- Cannot register or unregister without teacher login

## Security Note
⚠️ This is a simplified authentication system for demonstration purposes. In production:
- Use proper password hashing (bcrypt, argon2, etc.)
- Use HTTPS for all communications
- Implement proper session expiration
- Add CSRF protection
- Consider using a proper database instead of in-memory storage
