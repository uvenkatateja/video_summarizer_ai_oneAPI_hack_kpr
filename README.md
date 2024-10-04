# Secure_Chat_AI_oneAPI_hack_kpr

# Video Summarizer

This project is a Python-based tool that summarizes YouTube videos using the transcript. It provides features such as text summarization, PDF generation, and text-to-speech functionality.

## Features

- Extract video ID from YouTube links
- Fetch video transcripts
- Summarize video content
- Generate PDF summaries
- Text-to-speech for summaries

## Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.7+
- pip (Python package manager)

## Installation

1. Clone the repository:

   git clone https://github.com/yourusername/youtube-summarizer.git
   cd youtube-summarizer

2. Install the required packages:

   pip install -r requirements.txt

## Usage

1.  Import the necessary functions from youtube_summarizer.py:

    python
    from youtube_summarizer import extract_video_id, summarize_transcript, generate_pdf, speak_text

2.  Use the functions as needed in your application. Here's a basic example:

    python

    # Example usage

    video_link = "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
    video_id = extract_video_id(video_link)

    if video_id:
    transcript = YouTubeTranscriptApi.get_transcript(video_id)
    transcript_text = ' '.join([t['text'] for t in transcript])
    summary = summarize_transcript(transcript_text)

        print("Summary:", summary)

        pdf_file = generate_pdf(summary)
        print(f"PDF generated: {pdf_file}")

        speak_text(summary)

    else:
    print("Invalid YouTube link")

## Functions

- extract_video_id(link): Extracts the video ID from a YouTube link.
- summarize_transcript(transcript_text): Summarizes the given transcript text.
- chunk_text(text, max_length=1024): Splits text into smaller chunks for processing.
- generate_pdf(summary_text): Generates a PDF file containing the summary.
- speak_text(text): Reads the given text aloud using text-to-speech.

## Acknowledgments

- YouTube Transcript API
- Hugging Face Transformers
- pyttsx3 for text-to-speech functionality
- FPDF for PDF generation
