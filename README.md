🏦 Loan Advisory Chatbot

A conversational AI system that helps users explore and apply for loans intelligently.
It provides real-time eligibility checks, EMI calculations, and integrates with WhatsApp for seamless accessibility.

✨ Features

      💬 Conversational AI for loan advisory services

      ⚡ Real-time loan eligibility assessment using structured financial data

      🧮 EMI calculator and affordability analyzer

      💌 WhatsApp integration via Twilio API

      🌍 Multilingual support powered by Sarvam AI

      🧠 Google Gemini API + LangChain for AI-driven reasoning

      🗄️ PostgreSQL for secure financial data storage

      ☁️ AWS S3 for data accessibility and document uploads

🧰 Prerequisites

      Before you begin, make sure you have:

      Python 3.x

      PostgreSQL

      Ngrok
      (for local Twilio testing)

      API credentials for:

      Twilio

      Google Gemini

      AWS S3

⚙️ Installation

1. Clone the repository
   git clone https://github.com/duy098357/loan-chatbot.git
   cd loan-chatbot

2. Create and activate a virtual environment
   python -m venv venv
   venv\Scripts\activate     # On Windows
   # or
   source venv/bin/activate  # On macOS/Linux

3. Install dependencies
   pip install -r requirements.txt

4. Set up environment variables

   Create a file named .env in the project root:

      POSTGRES_HOST=your_host
      POSTGRES_PORT=5432
      POSTGRES_DB=my_database
      POSTGRES_USER=postgres
      POSTGRES_PASSWORD=your_password

      TWILIO_ACCOUNT_SID=your_twilio_sid
      TWILIO_AUTH_TOKEN=your_twilio_auth_token

      GOOGLE_GEMINI_API_KEY=your_api_key

      AWS_ACCESS_KEY_ID=your_aws_access_key
      AWS_SECRET_ACCESS_KEY=your_aws_secret_key
      AWS_REGION=your_aws_region
      S3_BUCKET_NAME=your_s3_bucket_name

🚀 Running the App Locally
      1. Start your Flask backend
      python app.py

      2. Expose it via Ngrok (for Twilio webhooks)
      ngrok http 5000


      Copy the public Ngrok URL and paste it in your Twilio WhatsApp sandbox configuration.

🌐 Deployment (Vercel)

      Push your project to GitHub

      Go to Vercel

      Click “New Project” → “Import Git Repository”

      Set your environment variables in Vercel Dashboard → Settings → Environment Variables

      Deploy 🚀

      Example vercel.json
      {
      "builds": [
         { "src": "app.py", "use": "@vercel/python" }
      ],
      "routes": [
         { "src": "/(.*)", "dest": "app.py" }
      ]
      }

🧠 Technologies Used

   Category	Technology
   Backend	Flask
   AI Integration	Google Gemini API, LangChain
   Messaging	Twilio (WhatsApp API)
   Database	PostgreSQL
   Cloud Storage	AWS S3
   Environment Management	Python Dotenv
   Testing	Ngrok

🧾 License

This project is licensed under the MIT License — feel free to use and modify it for your own projects.