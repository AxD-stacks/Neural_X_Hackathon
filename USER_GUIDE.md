# AI Learning System - User Guide

## Quick Start

### Installation
1. Run the setup script:
   - **Windows**: Double-click `setup.bat`
   - **Mac/Linux**: Run `./setup.sh`

2. Edit `.env` file with your API keys:
   ```
   ANTHROPIC_API_KEY=your-key-here
   YOUTUBE_API_KEY=your-key-here  # Optional
   ```

3. Start the application:
   ```bash
   python app.py
   ```

4. Open browser: `http://localhost:5000`

## Feature Walkthroughs

### 1. Uploading Documents

**Supported Formats:**
- PDF (.pdf)
- Word Documents (.docx)
- Text Files (.txt)
- Markdown (.md)

**How to Upload:**
1. Navigate to "📁 Upload Document" section
2. Either:
   - Click the upload area and select a file
   - Drag and drop a file onto the upload area
3. Wait for processing confirmation
4. You'll see file details once successful

**Tips:**
- Maximum file size: 16MB
- For best results, use well-formatted documents
- PDFs should have selectable text (not scanned images)

### 2. Document Summary

**Purpose:** Get a quick overview of your document's main points

**How to Use:**
1. Upload a document first
2. Go to "📝 Summary" section
3. Click "Generate Summary"
4. Wait 10-30 seconds for AI processing
5. Read the comprehensive summary

**What You Get:**
- Main topics covered
- Key concepts and definitions
- Important points and takeaways
- Structured with headings and bullet points

**Best For:**
- Quick review before exams
- Understanding new material
- Identifying important concepts
- Time-saving study technique

### 3. Interactive Quiz

**Purpose:** Test your knowledge with multiple-choice questions

**How to Use:**
1. Upload a document
2. Go to "❓ Quiz" section
3. Configure quiz settings:
   - **Number of Questions**: 5, 10, 15, or 20
   - **Difficulty**: Easy, Medium, or Hard
4. Click "Generate Quiz"
5. Answer each question by clicking an option
6. Click "Submit Quiz" when done

**Features:**
- Instant feedback on answers
- Explanations for correct answers
- Score percentage calculation
- Visual indicators (correct/incorrect)

**Study Tips:**
- Start with easy difficulty to build confidence
- Take the same quiz multiple times
- Read all explanations, even for correct answers
- Use quiz to identify weak areas

### 4. Mock Test

**Purpose:** Simulate real exam conditions with varied question types

**How to Use:**
1. Upload a document
2. Go to "📋 Mock Test" section
3. Click "Generate Mock Test"
4. Complete all sections:
   - **Multiple Choice Questions**: Select one answer
   - **True/False**: Click True or False
   - **Short Answer**: Type your response
5. Submit test to see results

**Features:**
- 20-25 questions total
- Multiple question types
- Point-based scoring
- Organized into sections
- Sample answers for short questions

**Test-Taking Tips:**
- Read questions carefully
- Manage your time (60-minute timer)
- Answer all questions
- Review explanations after submission

### 5. Mind Map

**Purpose:** Visual representation of concepts and relationships

**How to Use:**
1. Upload a document
2. Go to "🧠 Mind Map" section
3. Click "Generate Mind Map"
4. Explore the hierarchical structure

**Structure:**
- **Central Topic**: Main subject
- **Main Branches**: 4-6 major themes
- **Subtopics**: Supporting concepts
- **Key Points**: Detailed information

**Learning Benefits:**
- Better retention through visualization
- Understanding concept relationships
- Quick reference guide
- Ideal for visual learners

**How to Use Effectively:**
- Print or screenshot for study notes
- Use as a pre-study overview
- Reference during review sessions
- Create your own expanded versions

### 6. AI Tutor Chatbot

**Purpose:** Get personalized explanations and answers

**How to Use:**
1. Upload a document (optional but recommended)
2. Go to "💬 AI Tutor" section
3. Type your question in the input box
4. Press Enter or click "Send"
5. Read the AI's response
6. Ask follow-up questions

**Sample Questions:**
- "Explain [concept] in simple terms"
- "What's the difference between X and Y?"
- "Can you give me an example of [topic]?"
- "How does [concept] relate to [concept]?"
- "What are the main points about [topic]?"

**Tips for Better Responses:**
- Be specific in your questions
- Ask for examples or clarification
- Request different explanation styles
- Use it to prepare for exams
- Ask about real-world applications

**Use Cases:**
- Clarifying confusing concepts
- Getting different perspectives
- Preparing answers for discussions
- Deep diving into topics
- Learning at your own pace

### 7. Video Resources

**Purpose:** Find educational videos related to your topic

**How to Use:**

**Option 1: Manual Search**
1. Go to "🎥 Video Resources" section
2. Enter a search query (e.g., "photosynthesis explained")
3. Click "Search"
4. Browse video results
5. Click any video to watch on YouTube

**Option 2: Auto-Search**
1. Upload a document first
2. Go to "🎥 Video Resources" section
3. Click "Auto-Search from Document"
4. AI extracts the main topic and searches automatically

**Video Information Shown:**
- Thumbnail image
- Video title
- Channel name
- Description preview

**Learning Benefits:**
- Multiple learning modalities
- Different teaching styles
- Visual demonstrations
- Alternative explanations
- Supplementary material

## Advanced Tips

### Effective Study Workflow

1. **Initial Learning:**
   - Upload course material
   - Generate and read summary
   - Watch recommended videos

2. **Active Recall:**
   - Take the quiz (easy difficulty)
   - Use AI tutor for unclear concepts
   - Review mind map

3. **Deep Understanding:**
   - Retake quiz (medium/hard)
   - Ask detailed questions to AI tutor
   - Take mock test

4. **Exam Preparation:**
   - Review mind map
   - Take mock test under timed conditions
   - Focus on weak areas identified

### Maximizing AI Tutor

**For Concept Understanding:**
- "Explain [X] as if I'm 10 years old"
- "What's the analogy for [concept]?"
- "Walk me through [process] step by step"

**For Exam Prep:**
- "What are the most important points about [topic]?"
- "What questions might appear on an exam about [X]?"
- "Help me remember [concept] with a mnemonic"

**For Application:**
- "Give me a real-world example of [concept]"
- "How is [X] used in [field]?"
- "What are the practical implications of [theory]?"

### Study Session Templates

**Quick Review (15 minutes):**
1. Read summary (5 min)
2. Review mind map (5 min)
3. Quick quiz - 5 questions (5 min)

**Deep Study (1 hour):**
1. Read document (20 min)
2. Generate and review summary (10 min)
3. Take 10-question quiz (15 min)
4. Chat with AI tutor about unclear points (15 min)

**Exam Preparation (2 hours):**
1. Review mind map (15 min)
2. Watch 2-3 videos (30 min)
3. Take mock test (60 min)
4. Review wrong answers with AI tutor (15 min)

## Troubleshooting

### Common Issues

**"No document uploaded" error:**
- Solution: Upload a document in the Upload section first

**Quiz/Test not generating:**
- Check internet connection
- Verify API keys are set correctly
- Try with a smaller document
- Check console for errors

**Videos not showing:**
- YouTube API key required
- Check API quota limits
- Try manual search instead

**Slow response times:**
- Large documents take longer
- Split large files into sections
- Check internet speed
- API may be experiencing high traffic

### Best Practices

1. **Document Quality:**
   - Use clear, well-formatted documents
   - Avoid scanned PDFs (use OCR first)
   - Remove unnecessary content

2. **Session Management:**
   - Upload document once per session
   - Generate content as needed
   - Refresh page if encountering issues

3. **Privacy:**
   - Don't upload sensitive information
   - Remember: uploaded content is sent to AI services
   - Clear session when done on shared computers

## Keyboard Shortcuts

- **Chat Input**: Press `Enter` to send message
- **File Upload**: `Ctrl+Click` upload area to select file
- **Navigation**: Use sidebar to switch between sections

## Getting Help

If you encounter issues:
1. Check this user guide
2. Review README.md for technical details
3. Check console logs (F12 in browser)
4. Verify API keys are correctly set
5. Restart the application

## System Requirements

- **Browser**: Modern browser (Chrome, Firefox, Safari, Edge)
- **Internet**: Required for AI features
- **Screen**: Minimum 1024x768 resolution
- **JavaScript**: Must be enabled

## Privacy & Data

- Files are processed server-side
- Content is sent to Anthropic API for processing
- No data is permanently stored
- Session data cleared on browser close
- Use environment variables for API keys (never hardcode)

---

**Happy Learning!** 🎓

For more information, see README.md or contact support.
