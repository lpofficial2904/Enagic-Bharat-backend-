# Enagic Bharat Backend

Standalone backend for the Enagic Bharat contact/demo form.

## Local setup

```bash
cd backend
npm install
copy .env.example .env
npm run dev
```

Update `.env` with your real SMTP values before testing email.

## API

`POST /api/contact`

Required JSON body:

```json
{
  "name": "Customer Name",
  "email": "customer@example.com",
  "phone": "+91 98765 43210",
  "city": "Full address",
  "pincode": "302020",
  "timeSlot": "10:00 AM - 12:00 PM",
  "message": "I want a demo"
}
```

## Live deployment

Deploy this `backend` folder on a Node hosting service such as Render, Railway, VPS, or any host that supports Node.js.

Set these environment variables on the backend host:

```bash
PORT=5000
NODE_ENV=production
FRONTEND_URL=https://your-live-website.com
SMTP_HOST=smtp.gmail.com
SMTP_PORT=465
SMTP_SECURE=true
SMTP_USER=your-gmail-address@gmail.com
SMTP_PASS=your-gmail-app-password
CONTACT_TO_EMAIL=enagicbharat1974@gmail.com
CONTACT_FROM_EMAIL=enagicbharat1974@gmail.com
```

Then set this on the frontend hosting service:

```bash
VITE_API_BASE_URL=https://your-backend-domain.com
```
