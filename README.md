# Context-Aware Travel AI Bot 🤖✈️

An intelligent travel planning chatbot powered by the Gemini API that provides context-aware, multi-turn conversations to help users plan their perfect trip with real-time expense tracking and budget visualization.

## 🌟 Features

### AI-Powered Conversations
- **Multi-turn Dialogue**: Maintains conversational context across multiple exchanges
- **Context Awareness**: Remembers previous interactions to provide personalized recommendations
- **Custom Persona**: Travel-focused AI assistant with specialized knowledge
- **Intent Filtering**: Intelligently handles off-topic queries while staying focused on travel planning

### Travel Planning Tools
- **Destination Recommendations**: Get suggestions based on preferences, budget, and interests
- **Itinerary Planning**: Create detailed day-by-day travel plans
- **Activity Suggestions**: Discover local attractions, restaurants, and experiences
- **Travel Tips**: Receive practical advice on visas, weather, and local customs

### Expense Management
- **Real-time Expense Tracker**: Log and categorize travel expenses on the go
- **Dynamic Visualizations**: Interactive graphs showing budget breakdown
- **Budget Monitoring**: Track spending against your planned budget
- **Category Analysis**: Understand where your money is going (accommodation, food, transport, etc.)

### User Experience
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Smooth Animations**: Polished UI transitions and interactions
- **Fast Performance**: Client-side processing for instant responses
- **Clean Interface**: Intuitive design focused on usability

## 🚀 Tech Stack

- **HTML5** - Semantic structure and markup
- **CSS3** - Modern styling with animations and responsive design
- **JavaScript (ES6+)** - Core logic, API integration, and DOM manipulation
- **Gemini API** - Google's advanced AI for natural language processing
- **Chart.js / Canvas** - Dynamic data visualization for expense tracking

## 🛠️ Installation & Setup

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Gemini API key from [Google AI Studio](https://makersuite.google.com/app/apikey)

### Setup Instructions

1. **Clone the repository**
```bash
git clone https://github.com/JATIN-JAY/travel-ai-bot.git
cd travel-ai-bot
```

2. **Get your Gemini API Key**
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Sign in with your Google account
   - Create a new API key
   - Copy the key for the next step

3. **Configure API Key**

Open `config.js` or `script.js` and add your API key:
```javascript
const API_KEY = 'YOUR_GEMINI_API_KEY_HERE';
```

Alternatively, create a `config.js` file:
```javascript
export const CONFIG = {
  GEMINI_API_KEY: 'YOUR_GEMINI_API_KEY_HERE'
};
```

4. **Run the Application**

Simply open `index.html` in your web browser, or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using VS Code Live Server extension
# Right-click index.html → Open with Live Server
```

5. **Start Planning!**

Navigate to `http://localhost:8000` and start chatting with your AI travel assistant.

## 📁 Project Structure

```
travel-ai-bot/
├── index.html          # Main HTML structure
├── styles.css          # Styling and animations
├── script.js           # Core JavaScript logic
├── config.js           # API configuration (optional)
├── assets/
│   ├── icons/          # UI icons and graphics
│   └── images/         # Background images
└── README.md           # Project documentation
```

## 🎯 How It Works

### 1. Context Management
```javascript
// Maintains conversation history
conversationHistory = [
  { role: "user", content: "I want to visit Japan" },
  { role: "assistant", content: "Great choice! When are you planning to go?" }
];
```

### 2. Intent Filtering
The bot uses custom logic to detect and handle off-topic queries:
- Identifies travel-related intents (destinations, activities, budgets)
- Politely redirects non-travel queries back to planning
- Maintains context even when handling diversions

### 3. Expense Tracking
```javascript
// Real-time expense tracking
expenses = {
  accommodation: 5000,
  food: 2000,
  transport: 1500,
  activities: 3000
};
```

### 4. Gemini API Integration
```javascript
async function getChatResponse(userMessage) {
  const response = await fetch(`https://generativelanguage.googleapis.com/v1/models/gemini-pro:generateContent?key=${API_KEY}`, {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify({
      contents: [{ parts: [{ text: userMessage }] }]
    })
  });
  return await response.json();
}
```

## 💡 Usage Examples

### Planning a Trip
```
User: I want to plan a 5-day trip to Thailand
Bot: Wonderful! Thailand is an amazing destination. What's your budget for this trip?
User: Around $1500
Bot: Perfect! With $1500, you can have a great experience. Which cities are you interested in - Bangkok, Phuket, or Chiang Mai?
```

### Tracking Expenses
```
User: Add $50 for dinner at a local restaurant
Bot: Added $50 to food expenses. Your total food budget is now $150 out of $400 allocated.
```

### Getting Recommendations
```
User: What should I do in Kyoto?
Bot: Kyoto is rich in culture! I recommend visiting Fushimi Inari Shrine, exploring the Bamboo Grove in Arashiyama, and experiencing a traditional tea ceremony.
```

## 🎨 Features in Detail

### Custom Persona
The AI is configured with a travel expert persona that:
- Provides knowledgeable destination advice
- Suggests budget-friendly options
- Offers cultural insights and travel tips
- Maintains a friendly, enthusiastic tone

### Responsive Design
- **Mobile-First**: Optimized for smartphones and tablets
- **Flexible Layouts**: Adapts to different screen sizes
- **Touch-Friendly**: Large tap targets for mobile users
- **Fast Loading**: Minimal dependencies for quick load times

### Data Visualization
- **Pie Charts**: Budget allocation by category
- **Bar Graphs**: Daily expense tracking
- **Progress Bars**: Budget utilization indicators
- **Real-time Updates**: Instant visual feedback on changes

## 🔐 Security Notes

- Never commit your API key to version control
- Use environment variables or config files in `.gitignore`
- Consider implementing rate limiting for production
- Add API key rotation for enhanced security

## 🚧 Future Enhancements

- [ ] Multi-language support for international travelers
- [ ] Integration with flight and hotel booking APIs
- [ ] Weather forecast integration
- [ ] Offline mode with cached responses
- [ ] Export itineraries to PDF
- [ ] Currency conversion for international trips
- [ ] Collaborative trip planning for groups
- [ ] Integration with maps for location visualization

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👤 Author

Jatin Jay Singh
- GitHub: [@JATIN-JAY](https://github.com/JATIN-JAY)
- LinkedIn: [Jatin Jay Singh](https://www.linkedin.com/in/jatin-jay-singh-788088349/)

## 🙏 Acknowledgments

- Google Gemini API for powerful AI capabilities
- Travel planning inspiration from various travel apps
- Community feedback and contributions

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Reach out via LinkedIn

---

⭐ If you find this project helpful, please consider giving it a star!

Happy Travels! 🌍✈️
