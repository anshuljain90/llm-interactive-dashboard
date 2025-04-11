# LLM Interactive Dashboard

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![React](https://img.shields.io/badge/React-18.x-61DAFB.svg?logo=react)](https://reactjs.org/)

A natural language-powered dashboard system that uses Large Language Models to transform text prompts into dynamic visualizations and data insights. Simply describe what you want to see, and the AI will generate the appropriate visualization.

![Screenshot of the application](https://via.placeholder.com/800x450.png?text=LLM+Interactive+Dashboard+Screenshot)

## 🌟 Features

- **Natural Language Interface**: Type requests in plain English
- **AI-Powered Query Generation**: Automatically converts text to database queries
- **Dynamic Visualization**: Creates appropriate charts based on data and intent
- **Multiple Visualization Types**: Supports line charts, bar charts, pie charts, and tables
- **Contextual Prompts**: Suggests example prompts to help users get started

## 🚀 Quick Start

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn

### Installation

1. Clone this repository
   ```bash
   git clone https://github.com/yourusername/llm-interactive-dashboard.git
   cd llm-interactive-dashboard
   ```

2. Install dependencies
   ```bash
   npm install
   # or
   yarn install
   ```

3. Add your LLM API key
   ```bash
   # Create a .env file in the root directory and add:
   REACT_APP_OPENAI_API_KEY=your_api_key_here
   ```

4. Start the development server
   ```bash
   npm start
   # or
   yarn start
   ```

5. Open your browser and navigate to `http://localhost:3000`

## 🧠 How It Works

1. **User enters a natural language prompt** (e.g., "Show me sales trends by month for 2023")
2. **The LLM processes the request** and converts it to structured query parameters
3. **The application fetches relevant data** based on the interpreted request
4. **Dynamic visualization** renders the appropriate chart type
5. **Results are displayed** with title and context information

## 📊 Example Prompts

- "Show me sales trends by month for 2023"
- "Create a bar chart of top 5 products by revenue"
- "Display customer satisfaction ratings for Q1 in a pie chart"
- "Compare monthly expenses vs budget in a table"

## 🛠️ Technologies Used

- **React**: Frontend framework
- **Recharts**: Data visualization library
- **OpenAI API**: LLM integration (can be replaced with other LLM providers)
- **CSS**: Custom styling

## 🧩 Project Structure

```
src/
├── components/
│   ├── Dashboard.jsx       # Main dashboard container
│   ├── PromptInput.jsx     # User input for natural language queries
│   ├── Visualization.jsx   # Chart rendering component
│   └── LoadingIndicator.jsx # Loading animation
├── services/
│   ├── llmService.js       # API calls to the LLM
│   └── dataService.js      # Mock database and data operations
├── utils/
│   ├── promptTemplates.js  # System prompts for the LLM
│   └── visualizationHelpers.js # Formatting utilities
├── App.jsx                 # Main application component
└── index.js                # Entry point
```

## 🔧 Configuration

The application can be configured through environment variables:

- `REACT_APP_OPENAI_API_KEY`: Your OpenAI API key
- `REACT_APP_LLM_MODEL`: The specific model to use (default: "gpt-4")
- `REACT_APP_API_ENDPOINT`: Optional override for API endpoint

## 🚧 Extending the Project

### Adding New Data Sources

1. Update the mock database in `dataService.js` with new data sets
2. Add a new query type to handle the data retrieval
3. Update the system prompt template to inform the LLM about the new data

### Supporting More Visualization Types

1. Extend the `renderChart()` function in `Visualization.jsx`
2. Add corresponding data formatting logic in the visualization helpers
3. Update the system prompt to inform the LLM about the new visualization option

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👏 Acknowledgements

- This project was created as a learning resource for GenAI application development
- Inspired by modern natural language interfaces to databases and visualization systems
- Thanks to the React and OpenAI communities for their excellent documentation

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check [issues page](https://github.com/yourusername/llm-interactive-dashboard/issues).

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
