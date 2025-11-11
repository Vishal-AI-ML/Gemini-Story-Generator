# 📖 AI Story Generator - Image-to-Story with Voice Narration
Transform your images into captivating stories! Upload 1-10 images, select a genre, and let Google Gemini AI craft a complete narrative with voice narration.

## ✨ Key Features

### 🎭 **7 Story Genres**
- **Comedy** - Humorous tales with funny twists
- **Thriller** - Edge-of-your-seat suspense with shocking reveals
- **Fairy Tale** - Magical adventures with timeless charm
- **Sci-Fi** - Futuristic narratives with technological wonders
- **Mystery** - Detective stories with clues and solutions
- **Adventure** - Epic journeys with daring exploits
- **Morale** - Meaningful stories with life lessons

### 🤖 **Advanced AI Capabilities**
- **Multi-Image Processing** - Connects 1-10 images into coherent narratives
- **Context-Aware Generation** - Understands relationships between images
- **Genre-Specific Formatting** - Adds moral lessons, plot twists, or mystery solutions
- **Indian Context** - Uses Indian names, places, and cultural references
- **Structured Output** - 4-5 paragraph stories with clear beginnings and endings

### 🎙️ **Voice Narration**
- **Text-to-Speech** - Automatic story narration using Google TTS
- **Downloadable Audio** - Save and share your narrated stories
- **Natural Voice** - Clear English pronunciation

### 🖼️ **Smart Image Handling**
- Supports PNG, JPG, JPEG formats
- Visual preview of uploaded images
- Automatic image ordering in story flow
- Responsive grid layout

## 🛠️ Technology Stack

- **AI Model:** Google Gemini 2.0 Flash
- **Frontend:** Streamlit
- **Text-to-Speech:** gTTS (Google Text-to-Speech)
- **Image Processing:** Pillow (PIL)
- **Language:** Python 3.8+

## 📋 Prerequisites

- Python 3.8 or higher
- Google Gemini API key
- Internet connection (for API calls)

## 🚀 Installation

1. **Clone the repository**
```bash
git clone https://github.com/Vishal-AI-ML/Gemini-Story-Generator.git
cd Gemini-Story-Generator
```

2. **Create virtual environment**
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Set up environment variables**

Create a `.env` file in the root directory:
```env
GOOGLE_API_KEY=your_gemini_api_key_here
```

## 🎯 Usage

1. **Start the application**
```bash
streamlit run app.py
```

2. **Generate your story**
   - Upload 1-10 images using the sidebar
   - Select your preferred story genre
   - Click "Generate Story and Narration"
   - Read the generated story
   - Listen to the AI narration

## 📁 Project Structure

```
Gemini-Story-Generator/
├── app.py                    # Streamlit UI and main logic
├── story_generator.py        # Core AI functions
├── .env                      # Environment variables (create this)
├── requirements.txt          # Python dependencies
└── README.md                # Project documentation
```

## 🔑 Core Functions

### `create_advanced_prompt(style)`
Generates genre-specific prompts with special formatting rules:
- **Morale stories:** Adds `[MORAL]:` section
- **Mystery stories:** Adds `[SOLUTION]:` section  
- **Thriller stories:** Adds `[TWIST]:` section

### `generate_story_from_images(images, style)`
- Sends images + prompt to Gemini 2.0 Flash
- Returns coherent 4-5 paragraph narrative
- Handles errors gracefully

### `narrate_story(story_text)`
- Converts text to natural speech using gTTS
- Returns BytesIO audio stream
- Supports English narration

## 📊 Technical Specifications

| Feature | Details |
|---------|---------|
| Max Images | 10 per story |
| Story Length | 4-5 paragraphs (200-400 words) |
| Genres | 7 distinct styles |
| Response Time | 5-15 seconds (depends on images) |
| Audio Format | MP3 via gTTS |
| Image Formats | PNG, JPG, JPEG |

## 🎨 Genre-Specific Features

### **Mystery Stories**
Automatically adds a `[SOLUTION]` section revealing:
- The culprit
- Key clues that solve the mystery
- Detective reasoning

### **Thriller Stories**
Includes a `[TWIST]` section with:
- Shocking final revelation
- Plot reversal
- Unexpected ending

### **Morale Stories**
Ends with a `[MORAL]` section containing:
- Single-sentence life lesson
- Ethical takeaway
- Universal wisdom

## 👤 Author

**Vishal Shivhare**
- GitHub: [@Vishal-AI-ML](https://github.com/Vishal-AI-ML)
- LinkedIn: [Vishal Shivhare](https://linkedin.com/in/vishal-shivhare-562508243)
- Email: vishalshivhare.ai@gmail.com

## 🙏 Acknowledgments

- Google Gemini for powerful AI capabilities
- OpenWeather, NewsAPI, and SerpAPI for data services
- Unsplash for beautiful imagery
- Streamlit for the amazing framework

