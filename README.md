# Chinese Vocabulary Flashcards

A simple, interactive flashcard web application for learning Chinese vocabulary from the new HSK 3.0 levels. Practice Chinese characters, Pinyin pronunciation, and English definitions with an intuitive, keyboard-friendly interface.

## Features

- 📚 **Complete HSK Vocabulary**: Includes vocabulary from HSK levels 1-4 (3,245 words total)
  - HSK Level 1: 500 words
  - HSK Level 2: 772 words
  - HSK Level 3: 973 words
  - HSK Level 4: 1,000 words
- 🌐 **NS Concepts**: Network States and related concepts (54 terms)
  - Philosophy & systems thinking
  - Blockchain & decentralization
  - Cryptography & privacy
  - AI & computation
  - Governance & urban design
  - Startups & policy

- 🎯 **Level Filtering**: Filter flashcards by specific HSK level or view all levels together

- 🔀 **Randomization**: Shuffle cards for varied practice sessions

- ⌨️ **Keyboard Navigation**:
  - `←` / `→` Arrow keys: Navigate between cards
  - `↑` / `↓` Arrow keys: Flip card
  - `Space` / `Enter`: Flip card

- 🤖 **Auto Mode**: 
  - Automatically advance through cards at adjustable speed (0.5s - 5.0s)
  - Two modes:
    - **Both**: Shows Chinese, flips to show Pinyin/English, then advances
    - **Just Chinese**: Shows only Chinese side, then advances (no flip)

- 🎨 **Modern UI**: Beautiful gradient design with smooth animations

- 📱 **Responsive**: Works on desktop and mobile devices

## Project Structure

```
chinese/
├── index.html          # Main application file (HTML, CSS, JavaScript)
├── server.py           # Simple HTTP server for local development
├── hsk1new.md          # HSK Level 1 vocabulary (500 words)
├── hsk2new.md          # HSK Level 2 vocabulary (772 words)
├── hsk3new.md          # HSK Level 3 vocabulary (973 words)
├── hsk4new.md          # HSK Level 4 vocabulary (1,000 words)
├── nsconcepts.md       # NS Concepts vocabulary (54 terms)
└── README.md           # This file
```

## Prerequisites

- Python 3.x (for running the local server)
- A modern web browser (Chrome, Firefox, Safari, Edge)

## Running Locally

### Option 1: Using the Python Server (Recommended)

1. **Navigate to the project directory**:
   ```bash
   cd /path/to/chinese
   ```

2. **Start the server**:
   ```bash
   python3 server.py
   ```

3. **Open your browser** and navigate to:
   ```
   http://localhost:8000
   ```

4. **Stop the server** by pressing `Ctrl+C` in the terminal

### Option 2: Using Python's Built-in HTTP Server

If `server.py` is not available, you can use Python's built-in server:

```bash
cd /path/to/chinese
python3 -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

### Option 3: Direct File Access

You can also open `index.html` directly in your browser, though some features may be limited due to CORS restrictions when loading the vocabulary files.

## Usage

1. **Select a Level**: Click on "ALL", "Level 1", "Level 2", "Level 3", "Level 4", or "NS Concepts" to filter vocabulary

2. **Navigate Cards**: 
   - Use the "Previous" and "Next" buttons
   - Or use arrow keys (`←` / `→`)

3. **Flip Cards**: 
   - Click on the flashcard
   - Press `Space` or `Enter`
   - Press `↑` or `↓` arrow keys

4. **Randomize**: Click the "🔀 Randomize" button to shuffle the order

5. **Auto Mode**:
   - Check the "Auto" checkbox to enable automatic advancement
   - Adjust the speed slider (0.5s - 5.0s)
   - Choose mode:
     - **Both**: Shows Chinese, flips to show answer, then advances
     - **Just Chinese**: Shows only Chinese, then advances

## Vocabulary Data

The vocabulary lists are sourced from the [new HSK 3.0 levels](https://www.chinesetest.cn/hsk) and are stored in tab-separated markdown files with the following format:

```
No	Chinese	Pinyin	English
1	爱	ài	love
2	爱好	ài hào	hobby
...
```

## Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (no frameworks required)
- **Server**: Python's `http.server` module
- **Data Format**: Tab-separated markdown files
- **Browser Compatibility**: Works in all modern browsers

## Keyboard Shortcuts

| Key | Action |
|-----|--------|
| `←` | Previous card |
| `→` | Next card |
| `↑` / `↓` | Flip card |
| `Space` / `Enter` | Flip card |

## Deployment

### Deploy to Vercel

This app is ready for deployment on Vercel. Follow these steps:

1. **Install Vercel CLI** (optional, for command-line deployment):
   ```bash
   npm i -g vercel
   ```

2. **Deploy via Vercel Dashboard**:
   - Go to [vercel.com](https://vercel.com)
   - Sign up or log in
   - Click "New Project"
   - Import your Git repository or upload the project folder
   - Vercel will automatically detect it as a static site
   - Click "Deploy"

3. **Deploy via CLI**:
   ```bash
   cd /path/to/chinese
   vercel
   ```
   Follow the prompts to deploy.

4. **Configuration**:
   - The `vercel.json` file is already configured
   - All necessary files (HTML, CSS, vocabulary markdown files) will be deployed
   - The app will work immediately after deployment

The app will be available at a URL like `https://your-project.vercel.app`

### Other Deployment Options

- **Netlify**: Similar to Vercel, just drag and drop the folder or connect a Git repo
- **GitHub Pages**: Push to a GitHub repo and enable Pages in settings
- **Any static hosting**: The app works as a static site on any hosting provider

## License

This project uses vocabulary data from the HSK 3.0 test syllabus. The vocabulary lists are provided for educational purposes.

## Credits

- Vocabulary data from [Chinese Tests Service Website](https://www.chinesetest.cn/hsk)
- HSK 3.0 vocabulary lists

## Contributing

Feel free to submit issues or pull requests if you'd like to improve the application!
