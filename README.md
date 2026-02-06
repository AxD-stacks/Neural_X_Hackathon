# AI-Native Learning System 🎓

A comprehensive AI-powered educational platform that helps users learn from documents through intelligent summarization, interactive quizzes, mock tests, mind maps, AI tutoring, and curated video resources.

## Features

### 📁 File Upload
- Supports multiple formats: PDF, DOCX, TXT, MD
- Drag-and-drop interface
- Automatic text extraction
- Max file size: 16MB

### 📝 AI-Powered Summary
- Generates comprehensive summaries of uploaded documents
- Extracts key concepts and main ideas
- Well-structured with headings and bullet points
- Powered by Claude Sonnet 4

### ❓ Interactive Quiz Generator
- Customizable number of questions (5-20)
- Three difficulty levels: Easy, Medium, Hard
- Multiple-choice questions with 4 options each
- Instant feedback with explanations
- Score tracking and percentage calculation

### 📋 Mock Test Creator
- Comprehensive test with multiple question types:
  - Multiple Choice Questions (MCQ)
  - True/False Questions
  - Short Answer Questions
- Organized into logical sections
- Point-based scoring system
- Detailed explanations for all answers
- Sample answers for short answer questions

### 🧠 Mind Map Generator
- Visual representation of document content
- Hierarchical structure with:
  - Central topic
  - Main branches (4-6)
  - Subtopics with key points
- Color-coded and easy to navigate
- Great for visual learners

### 💬 AI Tutor Chatbot
- Real-time conversation with AI
- Context-aware responses based on uploaded document
- Can answer questions, explain concepts, and provide examples
- Maintains chat history during session
- Natural language interaction

### 🎥 Video Search Integration
- Search YouTube for educational videos
- Auto-search based on document topic
- Displays video thumbnails, titles, and channels
- Direct links to watch videos
- Helps with multi-modal learning

## Installation

### Prerequisites
- Python 3.8 or higher
- Anthropic API key
- YouTube Data API v3 key (optional, for video search)

### Setup Steps

1. **Clone or download the project**
   ```bash
   cd ai-learning-system
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   
   Create a `.env` file or set environment variables:
   
   ```bash
   # Required
   export ANTHROPIC_API_KEY="your-anthropic-api-key-here"
   
   # Optional (for video search feature)
   export YOUTUBE_API_KEY="your-youtube-api-key-here"
   ```

   **Getting API Keys:**
   
   - **Anthropic API Key**: 
     1. Sign up at https://console.anthropic.com/
     2. Navigate to API Keys section
     3. Create a new API key
   
   - **YouTube API Key** (Optional):
     1. Go to Google Cloud Console: https://console.cloud.google.com/
     2. Create a new project or select existing
     3. Enable YouTube Data API v3
     4. Create credentials (API Key)

5. **Create necessary directories**
   ```bash
   mkdir uploads templates
   ```

6. **Run the application**
   ```bash
   python app.py
   ```

7. **Open in browser**
   ```
   http://localhost:5000
   ```

## Project Structure

```
ai-learning-system/
├── app.py                 # Main Flask application
├── templates/
│   └── index.html        # Frontend interface
├── uploads/              # Temporary file storage
├── requirements.txt      # Python dependencies
└── README.md            # This file
```

## Usage Guide

### 1. Upload a Document
- Click on the upload area or drag and drop your file
- Supported formats: PDF, DOCX, TXT, MD
- Wait for successful upload confirmation

### 2. Generate Summary
- Navigate to "Summary" section
- Click "Generate Summary"
- Review the AI-generated comprehensive summary

### 3. Create a Quiz
- Go to "Quiz" section
- Select number of questions and difficulty
- Click "Generate Quiz"
- Answer questions and submit for instant feedback

### 4. Take a Mock Test
- Navigate to "Mock Test"
- Click "Generate Mock Test"
- Complete all sections (MCQ, True/False, Short Answer)
- Submit to see your score and detailed explanations

### 5. View Mind Map
- Go to "Mind Map" section
- Click "Generate Mind Map"
- Explore the hierarchical visualization of concepts

### 6. Chat with AI Tutor
- Navigate to "AI Tutor" section
- Type your questions about the document
- Get instant, context-aware responses
- Ask follow-up questions for deeper understanding

### 7. Find Video Resources
- Go to "Video Resources" section
- Either:
  - Enter a custom search query and click "Search"
  - Click "Auto-Search from Document" to find relevant videos
- Click on video thumbnails to watch on YouTube

## API Endpoints

### POST `/upload`
Upload and process a document file.

**Request:** `multipart/form-data` with file

**Response:**
```json
{
  "success": true,
  "filename": "document.pdf",
  "content_length": 5000
}
```

### POST `/summarize`
Generate summary of uploaded document.

**Response:**
```json
{
  "summary": "Comprehensive summary text..."
}
```

### POST `/generate-quiz`
Create an interactive quiz.

**Request:**
```json
{
  "num_questions": 10,
  "difficulty": "medium"
}
```

**Response:**
```json
{
  "questions": [
    {
      "question": "What is...?",
      "options": ["A", "B", "C", "D"],
      "correct_answer": 0,
      "explanation": "Because..."
    }
  ]
}
```

### POST `/generate-mock-test`
Create a comprehensive mock test.

**Response:**
```json
{
  "test_name": "Test Title",
  "duration_minutes": 60,
  "sections": [...]
}
```

### POST `/generate-mindmap`
Generate mind map structure.

**Response:**
```json
{
  "central_topic": "Main Topic",
  "branches": [
    {
      "title": "Branch",
      "subtopics": [...]
    }
  ]
}
```

### POST `/chat`
Chat with AI tutor.

**Request:**
```json
{
  "message": "What is photosynthesis?"
}
```

**Response:**
```json
{
  "response": "Photosynthesis is..."
}
```

### POST `/search-videos`
Search for educational videos.

**Request:**
```json
{
  "query": "machine learning basics"
}
```

**Response:**
```json
{
  "videos": [
    {
      "title": "Video Title",
      "videoId": "abc123",
      "thumbnail": "url",
      "channelTitle": "Channel"
    }
  ]
}
```

## Customization

### Styling
Edit the `<style>` section in `templates/index.html` to customize:
- Color scheme
- Layout
- Fonts
- Animations

### AI Behavior
Modify the `system_prompt` in each endpoint function in `app.py` to:
- Change tone and style
- Adjust difficulty levels
- Customize output format
- Add specific instructions

### Features
Add new features by:
1. Creating new endpoint in `app.py`
2. Adding corresponding section in `index.html`
3. Creating navigation item
4. Implementing JavaScript handler

## Troubleshooting

### File Upload Issues
- Check file size (max 16MB)
- Verify file format is supported
- Ensure `uploads/` directory exists and has write permissions

### API Errors
- Verify `ANTHROPIC_API_KEY` is set correctly
- Check API key has sufficient credits
- Review console logs for detailed error messages

### Video Search Not Working
- Ensure `YOUTUBE_API_KEY` is set
- Verify YouTube Data API v3 is enabled in Google Cloud Console
- Check API quota hasn't been exceeded

### Performance Issues
- Large documents (>10,000 words) may take longer to process
- Consider splitting very large files
- Check your internet connection for API calls

## Security Considerations

⚠️ **Important Security Notes:**

1. **Never commit API keys** to version control
2. **Use environment variables** for sensitive data
3. **Implement rate limiting** for production use
4. **Add user authentication** for multi-user deployments
5. **Sanitize file uploads** to prevent malicious files
6. **Set up HTTPS** for production deployment

## Future Enhancements

Potential improvements:
- [ ] User accounts and authentication
- [ ] Save/export features for quizzes and tests
- [ ] Progress tracking and analytics
- [ ] Spaced repetition for flashcards
- [ ] Multi-language support
- [ ] Mobile app version
- [ ] Collaborative study features
- [ ] Integration with learning management systems (LMS)
- [ ] Voice-based interaction
- [ ] Advanced analytics and insights

## Technical Stack

- **Backend**: Flask (Python)
- **AI**: Anthropic Claude Sonnet 4
- **Frontend**: HTML5, CSS3, Vanilla JavaScript
- **File Processing**: PyPDF2, python-docx
- **Video Search**: YouTube Data API v3
- **Session Management**: Flask sessions

## License

This project is open source and available for educational purposes.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## Support

For questions or issues:
1. Check the troubleshooting section
2. Review API documentation
3. Check console logs for errors
4. Ensure all dependencies are properly installed

## Credits

Built with:
- Anthropic Claude API for AI capabilities
- YouTube Data API for video search
- Flask for web framework
- Various Python libraries for document processing

---

**Happy Learning! 🚀**
