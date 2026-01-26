# ai-youtube-automation
This project automates the creation of YouTube knowledge videos using AI. It takes a topic or concept as input, generates a clear avatar-based script, converts it into a short video with AI voice narration, and uploads it to a YouTube channel automatically using n8n workflows.
## **What This Automation Does**



1\. Detects a new lesson added in Google Sheets

2\. Sends lesson text to OpenAI to generate a short video script

3\. Sends the script to HeyGen to generate a talking-head video

4\. Uploads the video to YouTube

5\. Writes the video link back to Google Sheets



## **Tools \& Services Used**



1: Trigger: Google Sheets → Detect new lessons

2: Script: OpenAI API (ChatGPT) → Convert text to video script

3: Video: HeyGen → Combine voice \& script into video

4: Upload: YouTube / Host the video

5: Save Link: Google Sheets /Keep track of uploaded videos

6: Workflow: n8n → Automate the entire process

---

## **How to setup Credentials** 



This workflow does not include any Credentials. You must add your own credentials to make it work.



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

\- Set the upload mode to \*\*Unlisted\*\* for automatic uploads



---



## **How to Use This Workflow**



1\. Open n8n  

2\. Click \*\*Import Workflow\*\*  

3\. Upload the `workflow.json` file  

4\. Configure all required credentials (Google Sheets, OpenAI, HeyGen, YouTube)  

5\. Activate the workflow



---



\## ⚠️ Notes for Users



\- API keys are \*\*never included\*\* in the workflow for security reasons  

\- Free plans of HeyGen / OpenAI may have usage limits  

\- Always double-check that “Bearer” is not removed in HeyGen nodes  

\- Keep all credentials safe and do not share publicly  



---



\## 👤 Author



Created by an AI Automation Engineer using n8n.






