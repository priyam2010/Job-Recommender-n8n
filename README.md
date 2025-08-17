# Job-Recommender-n8n
## Features
1.Scheduled Trigger

2.Fetch Jobs

3.Normalize Listings – Standardizes job fields (title, company, location, description, URL, posted date).

4.Match Scoring – Compares your resume/profile skills against job descriptions using embeddings to compute a similarity score (0–100).

5.Cover Letter Generation – Uses Gemini API to generate tailored cover letters.

6.Google Sheets Integration – Stores job details, match scores, and cover letters in a Google Sheet.

## flowchart TD

    A[⏰ Scheduled Trigger 10AM IST] --> B[🔍 Fetch Jobs via SerpAPI / JSearch]
    
    B --> C[📝 Normalize Listings]
    
    C --> D[🤖 Match Scoring using Embeddings]
    
    D --> E[✍️ Cover Letter via Gemini API]
    
    E --> F[📄 Append to Google Sheets]
    
    F --> G[📧 Send Daily Email Summary]
