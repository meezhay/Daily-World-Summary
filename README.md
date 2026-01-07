# 📰 News Summary App

A modern web application that delivers daily news summaries in simple, easy-to-understand language. Stay informed without the complexity!

## ✨ Features

- **Daily News Summaries**: Get current day's news events summarized in simple language
- **Multi-Language Support**: Choose from 8 languages (English, Spanish, French, German, Italian, Portuguese, Arabic, Chinese)
- **Customizable Categories**: Select your news preferences from:
  - General
  - Business
  - Technology
  - Science
  - Health
  - Sports
  - Entertainment
- **Clean, Responsive UI**: Works beautifully on desktop and mobile devices
- **Easy to Understand**: News is simplified for better comprehension
- **Real-time Updates**: Refresh button to get the latest news anytime

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- (Optional) NewsAPI key for live news data

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Project-Ideas
   ```

2. **Install dependencies**
   ```bash
   npm run install-all
   ```
   This will install dependencies for both the server and client.

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```

   Edit `.env` and add your NewsAPI key (optional):
   ```
   NEWS_API_KEY=your_api_key_here
   PORT=5000
   ```

   > **Note**: You can get a free API key from [NewsAPI.org](https://newsapi.org/). If you don't provide an API key, the app will use mock data for demonstration.

### Running the Application

#### Development Mode

Run both server and client concurrently:
```bash
npm run dev
```

Or run them separately:

**Terminal 1 - Server:**
```bash
npm run server
```

**Terminal 2 - Client:**
```bash
npm run client
```

The application will be available at:
- Frontend: `http://localhost:3000`
- Backend API: `http://localhost:5000`

## 🎯 How to Use

1. **Open the app** in your browser at `http://localhost:3000`

2. **Select your preferences**:
   - Choose your preferred language from the dropdown
   - Select a news category that interests you

3. **Read the news**: Simplified summaries will be displayed in an easy-to-read card format

4. **Refresh**: Click the "Refresh" button to get the latest news

5. **Read more**: Click "Read full article →" on any card to view the complete story

## 🏗️ Project Structure

```
Project-Ideas/
├── server/                 # Backend Express server
│   ├── index.js           # Server entry point
│   ├── routes/
│   │   └── news.js        # News API routes
│   └── services/
│       ├── newsService.js     # News fetching logic
│       └── summaryService.js  # Text summarization
├── client/                # React frontend
│   ├── public/
│   │   └── index.html
│   └── src/
│       ├── components/    # React components
│       │   ├── Header.js
│       │   ├── PreferencesPanel.js
│       │   ├── NewsList.js
│       │   ├── NewsCard.js
│       │   └── LoadingSpinner.js
│       ├── App.js         # Main App component
│       └── index.js       # React entry point
├── package.json
└── README.md
```

## 🔧 API Endpoints

### Get Today's News
```
GET /api/news/today?language=en&category=general&country=us
```

### Get Available Categories
```
GET /api/news/categories
```

### Get Supported Languages
```
GET /api/news/languages
```

### Health Check
```
GET /api/health
```

## 🌍 Supported Languages

- English (en)
- Spanish (es)
- French (fr)
- German (de)
- Italian (it)
- Portuguese (pt)
- Arabic (ar)
- Chinese (zh)

## 📱 Responsive Design

The app is fully responsive and works on:
- Desktop computers
- Tablets
- Mobile phones

## 🛠️ Technologies Used

### Backend
- Node.js
- Express.js
- Axios
- Node-Cache
- NewsAPI

### Frontend
- React 18
- CSS3 (with modern features)
- Axios

## 🔐 Security Notes

- Never commit your `.env` file
- Keep your API keys secure
- The `.gitignore` file is configured to exclude sensitive files

## 🐛 Troubleshooting

### Port already in use
If port 5000 or 3000 is already in use, you can change them:
- Server: Edit `PORT` in `.env` file
- Client: Create a `.env` file in the `client` folder with `PORT=3001`

### No news appearing
- Check if your NewsAPI key is valid
- Ensure you have an internet connection
- The app will use mock data if NewsAPI is unavailable

### CORS errors
Make sure the `proxy` setting in `client/package.json` matches your server port.

## 📝 Future Enhancements

- Email/SMS notifications for daily summaries
- Save favorite news articles
- Share articles on social media
- Voice reading of summaries
- Offline mode with cached news
- User accounts for personalized experience

## 📄 License

MIT License - feel free to use this project for learning and development!

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 💡 Tips

- The app caches news for 1 hour to reduce API calls
- Mock data is available if you don't have an API key
- News is automatically summarized to be easy to understand
- Complex words are replaced with simpler alternatives

---

**Enjoy staying informed with simple, clear news summaries!** 📰✨
