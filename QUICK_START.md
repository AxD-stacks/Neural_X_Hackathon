# 🎓 AI Learning System - Quick Start

Welcome to your AI-Native Learning Platform! This system helps you learn from documents using cutting-edge AI technology.

## ⚡ Quick Setup (5 minutes)

### Step 1: Get Your API Key
1. Visit https://console.anthropic.com/
2. Sign up or log in
3. Create an API key
4. Copy it for the next step

### Step 2: Install

**Windows Users:**
```cmd
1. Double-click setup.bat
2. Wait for installation to complete
```

**Mac/Linux Users:**
```bash
chmod +x setup.sh
./setup.sh
```

### Step 3: Configure
1. Open `.env` file in a text editor
2. Replace `your-anthropic-api-key-here` with your actual API key
3. (Optional) Add YouTube API key for video search

### Step 4: Run
```bash
# Activate virtual environment
# Windows: venv\Scripts\activate
# Mac/Linux: source venv/bin/activate

# Run the app
python app.py
```

### Step 5: Use
Open your browser to: **http://localhost:5000**

## 🎯 Main Features

| Feature | Description | Use Case |
|---------|-------------|----------|
| 📝 **Summary** | AI-generated document summaries | Quick review & understanding |
| ❓ **Quiz** | Interactive multiple-choice questions | Self-testing & knowledge check |
| 📋 **Mock Test** | Comprehensive exam simulation | Exam preparation |
| 🧠 **Mind Map** | Visual concept mapping | Understanding relationships |
| 💬 **AI Tutor** | Chat with AI about topics | Q&A & clarification |
| 🎥 **Videos** | Curated educational videos | Multi-modal learning |

## 📚 Supported File Types
- PDF (.pdf)
- Word Documents (.docx)
- Text Files (.txt)
- Markdown (.md)

## 🚀 Typical Workflow

```
1. Upload Document → 2. Read Summary → 3. Watch Videos
                ↓
4. Take Quiz → 5. Ask AI Tutor → 6. Take Mock Test
                ↓
           7. Review Mind Map
```

## 💡 Pro Tips

1. **Start with Summary**: Get an overview before diving deep
2. **Use Mind Maps**: Great for visual learners
3. **Progressive Difficulty**: Start with easy quizzes, move to hard
4. **Active Learning**: Use AI Tutor to ask questions
5. **Video Learning**: Watch videos for concepts you find difficult
6. **Mock Tests**: Simulate real exam conditions for best prep

## 📖 Documentation

- **README.md**: Technical details & API documentation
- **USER_GUIDE.md**: Comprehensive feature walkthroughs
- **This file**: Quick reference & setup

## ⚙️ Configuration

### Required
- `ANTHROPIC_API_KEY`: For AI features (Required)

### Optional
- `YOUTUBE_API_KEY`: For video search feature
  - Get it from: https://console.cloud.google.com/
  - Enable YouTube Data API v3

## 🔧 Troubleshooting

**"Module not found" error:**
```bash
pip install -r requirements.txt
```

**"API key not set" error:**
- Check `.env` file exists
- Verify API key is correct
- Restart the application

**Files not uploading:**
- Check file size (max 16MB)
- Verify file format is supported

**Videos not showing:**
- Add YouTube API key to `.env`
- Or use manual search instead

## 🎨 Customization

### Change Colors
Edit the CSS in `templates/index.html` (lines 10-400)

### Modify AI Behavior
Edit system prompts in `app.py` for each feature

### Add Features
1. Add endpoint in `app.py`
2. Add section in `templates/index.html`
3. Add navigation item

## 🔒 Security Notes

⚠️ **Important:**
- Never share your API keys
- Don't commit `.env` to version control
- Use HTTPS in production
- Implement authentication for multi-user setups

## 📊 Example Use Cases

**For Students:**
- Exam preparation
- Quick chapter reviews
- Concept clarification
- Practice tests

**For Self-Learners:**
- New topic exploration
- Knowledge validation
- Structured learning paths
- Multi-format content

**For Teachers:**
- Create study materials
- Generate practice tests
- Assess comprehension
- Supplement lessons

## 🆘 Need Help?

1. Check **USER_GUIDE.md** for detailed instructions
2. Review **README.md** for technical details
3. Check browser console (F12) for errors
4. Verify API keys are set correctly

## 🎯 Next Steps

After setup, try this:
1. Upload a sample document (try a textbook chapter or article)
2. Generate a summary
3. Create a quiz with 5 questions
4. Chat with the AI tutor
5. Explore other features!

## 📈 System Requirements

- Python 3.8+
- Modern web browser
- Internet connection
- 100MB free disk space

## 🌟 Features Coming Soon

- Flashcard generation
- Progress tracking
- Spaced repetition
- Multi-document analysis
- Export to PDF
- Mobile app

---

**Ready to learn?** Start the app and upload your first document!

```bash
python app.py
```

Then visit: **http://localhost:5000**

**Happy Learning! 🚀**
