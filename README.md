# ai-youtube-automation
This project automates the creation of YouTube knowledge videos using AI. It takes a topic or concept as input, generates a clear avatar-based script, converts it into a short video with AI voice narration, and uploads it to a YouTube channel automatically using n8n workflows.

## **How This automation works**

1\. Detects a new lesson added in Google Sheets

2\. Sends lesson text to OpenAI to generate a short video script

3\. Sends the script to HeyGen to generate a talking-head video

4\. Uploads the video to YouTube

5\. Writes the video link back to Google Sheets

## Tools & Services Used

- Google Sheets – Lesson source and trigger
- OpenAI (ChatGPT) – Generate video scripts
- HeyGen – Create avatar-based talking-head videos
- YouTube – Host and publish videos
- n8n – Automate the entire workflow

## **How to setup Credentials** 

⚠️ This repository does not include any API keys or credentials for security reasons.


1️⃣ Google Sheet

\- Create a Google Service Account or use OAuth credentials  

\- Connect it to n8n → Google Sheets node → Access the sheet with lessons



2️⃣ OpenAI (ChatGPT)

\- Sign up at \[OpenAI](https://platform.openai.com/)  

\- Generate an API key  

\- Add it in n8n → OpenAI node → Credentials → API Key



3️⃣ HeyGen API

You need to add your HeyGen API key in \*\*two nodes\*\*:



1\. Generate Video (HeyGen) 

2\. Check Video Status (HeyGen)



&nbsp;How to Add Your API Key



Step 1: Open the n8n workflow and locate the two nodes mentioned above  



Step 2: Replace the placeholder in the \*\*Header Parameters → Value\*\*



-Generate Video (HeyGen) 

&nbsp;Replace:PASTE\_HEYGEN\_API\_KEY

&nbsp;with your actual API key



-Check Video Status (HeyGen) 

&nbsp;Replace: Bearer PASTE\_HEYGEN\_API\_KEY

&nbsp;with your actual API key \*\*but keep the word "Bearer" exactly as it is\*\*



&nbsp;Example: Bearer your key

> ⚠️ Important: Only replace the placeholder. Do not remove the word “Bearer” in the second node.



4️⃣ YouTube

\- Create or use a verified YouTube account  

\- Connect YouTube OAuth credentials in n8n  

## How to Use This Workflow

1. Download the `ai-youtube-automation.json` file from this repository.  

2. Open n8n.  

3. Click **Import Workflow**.  

4. Upload the downloaded `ai-youtube-automation.json` file.  

5. Configure all required credentials:
   - Google Sheets  
   - OpenAI (ChatGPT)  
   - HeyGen  
   - YouTube  

6. Activate the workflow.

## ⚠️ Notes for Users

- This workflow can be customized to match your specific use case.

- Videos are uploaded directly to the YouTube channel. Upload visibility (Public or Unlisted) can be adjusted in the YouTube node if required.

- API keys and credentials are not included for security reasons. Add your own credentials before running the workflow.

- Free plans of OpenAI or HeyGen may have usage limits or watermarks.

- Always test changes before using the workflow in a live environment.

- Do not remove the word **"Bearer"** when adding the HeyGen API key in the status check node.

 👤 Author
 Created by Inam Ullah, an AI Automation Developer







