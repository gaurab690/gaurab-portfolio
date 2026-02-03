# EmailJS Setup Instructions

## Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Sign up for a free account (allows 200 emails/month)

## Step 2: Create an Email Service
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail recommended)
4. Connect your Gmail account: gaurab.lamichhane777@gmail.com
5. Copy the **Service ID** (you'll need this)

## Step 3: Create an Email Template
1. Go to "Email Templates" in the dashboard
2. Click "Create New Template"
3. Use this template structure:
   - **Subject**: New Contact Form Message from {{from_name}}
   - **Content**:
     ```
     From: {{from_name}}
     Email: {{from_email}}
     
     Message:
     {{message}}
     ```
4. Save and copy the **Template ID**

## Step 4: Get Your Public Key
1. Go to "Account" → "General"
2. Copy your **Public Key**

## Step 5: Update the Code
Open `index.html` and replace these placeholders in the JavaScript section (around line 207):

1. Replace `YOUR_PUBLIC_KEY` with your EmailJS Public Key
2. Replace `YOUR_SERVICE_ID` with your Service ID
3. Replace `YOUR_TEMPLATE_ID` with your Template ID

Example:
```javascript
emailjs.init("abc123xyz"); // Your Public Key
...
emailjs.send('service_abc123', 'template_xyz789', templateParams)
```

## Testing
1. Fill out the contact form on your website
2. Submit the form
3. Check your email inbox (gaurab.lamichhane777@gmail.com)
4. You should receive the message!

## Features Included
- ✅ HTML5 form validation (required fields)
- ✅ Email format validation
- ✅ Visual success/error messages
- ✅ Button disabled during submission
- ✅ Form reset after successful submission
