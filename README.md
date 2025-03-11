# Social-Media-Short-Content-Automation
# Social Media Short Content Automation

## Overview
The **Social Media Short Content Automation** tool automates the process of generating, editing, and posting short-form content for platforms like Instagram Reels, TikTok, and YouTube Shorts. It uses AI to extract key highlights from long videos, generate captions, and create thumbnails, streamlining content creation.

## Features
- **Automated Highlight Extraction**: AI detects the most engaging parts of a video.
- **AI-Generated Captions**: Adds subtitles with customizable styles.
- **Thumbnail Creation**: Generates eye-catching thumbnails.
- **Multi-Platform Posting**: Automates uploads to social media platforms.
- **API Access**: Provides endpoints for seamless integration.

## Tech Stack
- **Backend**: FastAPI (Python)
- **AI Models**: LLMs/GenAI for captions and highlights
- **Frontend**: Optional (React/Vue.js for UI)
- **Storage**: Local/MongoDB/PostgreSQL (for metadata and processed files)
- **Processing**: FFMPEG, OpenCV
- **Social Media APIs**: Instagram, TikTok, YouTube

## Installation
```sh
# Clone the repository
git clone https://github.com/your-username/social-media-automation.git
cd social-media-automation

# Create and activate a virtual environment
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

# Install dependencies
pip install -r requirements.txt
```

## Usage
### 1. Run the FastAPI Server
```sh
uvicorn app.main:app --host 0.0.0.0 --port 8000 --reload
```
The API will be available at `http://localhost:8000/docs`

### 2. Process a Video
#### API Endpoint:
`POST /generate-content`

#### Request Body:
```json
{
  "video_url": "https://example.com/video.mp4",
  "duration": 30,
  "generate_captions": true,
  "generate_thumbnail": true,
  "post_to_social": true,
  "platforms": ["Instagram", "TikTok"]
}
```

#### Response:
```json
{
  "status": "success",
  "short_video_url": "https://your-storage.com/output.mp4",
  "thumbnail_url": "https://your-storage.com/thumbnail.jpg",
  "post_status": "uploaded"
}
```

## Customization
- Modify **caption styles** in `config/captions.json`
- Adjust **video processing parameters** in `config/settings.json`
- Connect custom **social media accounts** via API keys in `config/social.json`

## Contributing
1. Fork the repo & clone locally
2. Create a feature branch (`git checkout -b feature-name`)
3. Commit changes (`git commit -m 'Add feature'`)
4. Push to your fork & create a PR

## License
This project is licensed under the MIT License.

## Contact
For issues and support, open an issue on GitHub or contact mohansivatejakavvala2011@gmail.com.
