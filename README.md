🩺 Physician Notetaker - Medical NLP Pipeline
📌 Overview
This project builds an AI-powered NLP pipeline for medical transcription, summarization, sentiment analysis, and SOAP note generation. It processes doctor-patient conversations to extract key medical details, classify patient sentiment, and generate structured medical reports.

📌 Features
✅ Medical Named Entity Recognition (NER) – Extracts Symptoms, Diagnosis, Treatment, and Prognosis
✅ Text Summarization – Generates a structured medical report
✅ Keyword Extraction – Identifies key medical terms
✅ Sentiment Analysis – Classifies patient sentiment as Anxious, Neutral, or Reassured
✅ Intent Classification – Detects if the patient is Reporting Symptoms, Seeking Reassurance, or Having General Conversation
✅ SOAP Note Generation – Automatically formats a structured SOAP note

📌 Installation
1️⃣ Clone the Repository
git clone https://github.com/your-username/physician-notetaker.git
cd physician-notetaker
2️⃣ Install Dependencies

Note: If using a GPU, install torch and transformers with CUDA support for faster processing.

📌 Usage
Run the NLP Pipeline
Execute the following command to process a conversation transcript:
python main.py

📌 Example Input & Output
📍 Input Transcript

Patient: I had a car accident. My neck and back hurt a lot for four weeks.
Doctor: Did you receive treatment?
Patient: Yes, I had ten physiotherapy sessions, and now I only have occasional back pain.

📍 Output - Structured Summary (JSON)
{
  "Patient_Name": "Janet Jones",
  "Symptoms": ["Neck pain", "Back pain"],
  "Diagnosis": "Whiplash injury",
  "Treatment": ["Physiotherapy sessions", "Painkillers"],
  "Current_Status": "Occasional backache",
  "Prognosis": "Full recovery expected within six months"
}
📍 Output - Sentiment & Intent Analysis
{
  "Sentiment": "Reassured",
  "Intent": "Reporting symptoms"
}
📍 Output - SOAP Note
{
  "Subjective": {
    "Chief_Complaint": "Neck and back pain",
    "History_of_Present_Illness": "Patient had a car accident, experienced pain for four weeks, now occasional back pain."
  },
  "Objective": {
    "Physical_Exam": "Full range of motion in cervical and lumbar spine, no tenderness.",
    "Observations": "Patient appears in normal health."
  },
  "Assessment": {
    "Diagnosis": "Whiplash injury",
    "Severity": "Mild, improving"
  },
  "Plan": {
    "Treatment": "Continue physiotherapy, use pain relief medication as needed.",
    "Follow-Up": "Return if pain worsens or persists beyond six months."
  }
}

📌 Future Enhancements
🔹 Fine-tune BERT for medical sentiment analysis using MIMIC-III dataset
🔹 Deploy as a FastAPI/Flask API for real-time transcription & analysis
🔹 Use scispacy for improved medical entity extraction

🚀 Happy Coding! 🚀

