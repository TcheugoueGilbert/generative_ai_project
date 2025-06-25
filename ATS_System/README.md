# ATS Resume Expert

ATS Resume Expert is a Streamlit web application that leverages Google Gemini AI to analyze and evaluate resumes against job descriptions. It provides an Applicant Tracking System (ATS)-style review, including a percentage match, missing keywords, and professional feedback to help candidates optimize their resumes for specific roles.

## Features

- **Resume Upload:** Upload your resume in PDF format.
- **Job Description Input:** Paste or type the job description for the target role.
- **AI-Powered Analysis:** Uses Google Gemini's vision model to analyze the resume.
- **ATS Match Percentage:** Get a percentage match score between your resume and the job description.
- **Missing Keywords:** Identify important keywords missing from your resume.
- **Professional Feedback:** Receive strengths, weaknesses, and suggestions for improvement.

## How It Works

1. The user uploads a resume (PDF).
2. The app converts the first page of the PDF to an image and encodes it for AI processing.
3. The user provides a job description.
4. The app sends both the resume image and job description to Google Gemini for analysis.
5. The AI returns a detailed evaluation, including match percentage and feedback.

## Setup Instructions

### Prerequisites

- Python 3.8+
- [Google Gemini API access](https://ai.google.dev/)
- [Poppler](https://github.com/oschwartz10612/poppler-windows) (for PDF to image conversion)

### Installation

1. **Clone the repository:**
    ```sh
    git clone <https://github.com/TcheugoueGilbert/generative_ai_project>
    cd <generative_ai_project/ATS_System>
    ```

2. **Create and activate a virtual environment:**
    ```sh
    python -m venv genai-venv
    source genai-venv/Scripts/activate  # On Windows
    # or
    source genai-venv/bin/activate      # On macOS/Linux
    ```

3. **Install dependencies:**
    ```sh
    pip install -r requirements.txt
    ```

4. **Set up environment variables:**
    - Create a `.env` file in the project root with your Google API key:
      ```
      GOOGLE_API_KEY=your_google_api_key_here
      ```

5. **Install Poppler:**
    - Download and install Poppler for your OS.
    - Add the Poppler `bin` directory to your system PATH.

### Running the App

```sh
streamlit run app.py
```

Open the provided local URL in your browser to use the app.

## File Structure

```
.
├── app.py                # Main Streamlit application
├── requirements.txt      # Python dependencies
├── .env                  # Environment variables (not committed)
├── README.md             # Project documentation
└── ATS_System/           # (Optional) Additional app modules
```

## Dependencies

- streamlit
- python-dotenv
- pillow
- pdf2image
- google-generativeai

## Notes

- Only the first page of the resume PDF is analyzed.
- Ensure your Google API key has access to Gemini Pro Vision.
- For best results, use clear and well-formatted resumes.

## License

This project is licensed under the MIT License.

## Acknowledgements

- [Streamlit](https://streamlit.io/)
- [Google Gemini AI](https://ai.google.dev/)
- [pdf2image](https://github.com/Belval/pdf2image)
- [Pillow](https://python-pillow.org/)

---

Feel free to contribute or open issues for improvements!