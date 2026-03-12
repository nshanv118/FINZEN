# Render Environment Setup for FinZen

To fix the AI Chatbot error, you must add your Google Gemini API Key to your Render dashboard.

### Steps to Configure

1. **Get your API Key:** Go to the [Google AI Studio](https://aistudio.google.com/app/apikey) and copy your API key.
2. **Open Render Dashboard:** Navigate to your **FinZen** Web Service on Render.
3. **Environment Tab:** Click on the **Environment** link in the side menu.
4. **Add Variable:** Click **Add Environment Variable**.
   - **Key:** `GEMINI_API_KEY`
   - **Value:** `Paste_Your_Long_Key_Here`
5. **Save Changes:** Click **Save Changes**.
6. **Deploy:** Render should automatically start a new deployment. If not, click **Manual Deploy** -> **Deploy Latest Commit**.

### Why is this needed?
The `.env` file on your local machine is ignored by Git (via `.gitignore`) for security reasons. This avoids accidentally sharing your private keys on GitHub. In production (Render), you must provide these keys manually via their Environment Variables system.
