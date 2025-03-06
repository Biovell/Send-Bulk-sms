Bulk SMS Sender using Twilio & Firebase
📌 Overview
This project is a Bulk SMS Sender that allows users to send messages to multiple recipients using Twilio's SMS API. It is built with Firebase Cloud Functions and supports sending personalized messages efficiently.

🚀 Features
✅ Send bulk SMS to multiple phone numbers
✅ Uses Twilio API for SMS delivery
✅ Firebase Cloud Functions for backend processing
✅ Secure API endpoint for sending messages
✅ JSON-based request handling
✅ Logs response status for debugging

🛠️ Technologies Used
Firebase Cloud Functions (Server-side execution)
Twilio API (SMS delivery)
Node.js & Express.js (Backend logic)
cURL / Postman (For API testing)
📂 Project Structure
bash
Copy
Edit
📦 BulkSMS  
 ┣ 📂 functions  
 ┃ ┣ 📜 index.js  # Main Firebase Cloud Function  
 ┃ ┣ 📜 package.json  # Dependencies  
 ┃ ┣ 📜 .env  # Twilio API credentials  
 ┃ ┗ 📜 README.md  # Project documentation  
 ┣ 📂 scripts  
 ┃ ┣ 📜 send_sms.sh  # cURL script for testing  
 ┃ ┗ 📜 send_sms.py  # Python script for sending SMS  
 ┗ 📜 README.md  # Project Overview  
🔧 Setup & Installation
1️⃣ Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/bulk-sms.git  
cd bulk-sms/functions
2️⃣ Install Dependencies
bash
Copy
Edit
npm install
3️⃣ Configure Environment Variables
Create a .env file inside the functions directory and add your Twilio credentials:

ini
Copy
Edit
TWILIO_ACCOUNT_SID=your_account_sid  
TWILIO_AUTH_TOKEN=your_auth_token  
TWILIO_PHONE_NUMBER=your_twilio_number
4️⃣ Deploy Firebase Functions
bash
Copy
Edit
firebase deploy --only functions
5️⃣ Send SMS using cURL
bash
Copy
Edit
curl -X POST "http://127.0.0.1:5001/bulksms100/us-central1/sendBulkSms" \
     -H "Content-Type: application/json" \
     -d '{
          "to": ["+233241676978", "+233279940200"],
          "message": "Hello from Bulk SMS!"
         }'
📌 Notes
If using Twilio Trial Account, you must verify recipient numbers first.
For production use, upgrade your Twilio account to remove restrictions.
Consider alternative SMS providers like Africa's Talking or Nexmo (Vonage) if needed.
