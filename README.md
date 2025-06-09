# URL
https://github.com/pleabargain/ollama-marketing-app

# Why?
I saw a guy selling this as an app. I said to myself: that's trivial. And it was. And it still is!


# Marketing Automation Workflow Generator

A web-based application that generates personalized marketing automation workflows using AI-powered language models through the Ollama platform.

![Image](https://github.com/user-attachments/assets/5e6567dd-46e2-4a5c-a529-672827daa21e)

## Purpose

This HTML application helps businesses create comprehensive marketing automation workflows by leveraging artificial intelligence. Users input their business details, target customer persona, challenges, and unique selling proposition, and the AI generates a detailed, actionable marketing automation strategy.

## Features

- **AI-Powered Workflow Generation**: Creates detailed marketing automation workflows using the llama3.2 language model
- **Real-time Connection Status**: Monitors Ollama server connection and model availability
- **Pre-loaded Sample Data**: Includes realistic test data for quick testing and demonstration
- **Responsive Design**: Modern, mobile-friendly interface with gradient backgrounds and smooth animations
- **Error Handling**: Comprehensive error messages and troubleshooting guidance
- **Input Validation & Sanitization**: Robust input validation with real-time feedback and security measures

## What It Generates

The application creates marketing automation workflows that include:

1. **Awareness Stage Tactics** - Strategies to attract potential customers
2. **Consideration Stage Nurturing** - Methods to engage and educate prospects
3. **Decision Stage Conversion** - Techniques to convert leads into customers
4. **Post-Purchase Retention** - Strategies for customer retention and advocacy
5. **Content Recommendations** - Specific content suggestions for each stage
6. **Automation Triggers** - Recommended timing and triggers for automated actions
7. **Key Metrics** - Important KPIs to track workflow effectiveness

## About Ollama

### What is Ollama?

Ollama is a powerful, open-source platform that allows you to run large language models (LLMs) locally on your computer. It provides a simple API interface for interacting with various AI models without requiring cloud services or external API keys.

### Key Benefits of Ollama:

- **Privacy**: All processing happens locally on your machine
- **No API Costs**: No per-request charges or subscription fees
- **Offline Capability**: Works without internet connection once models are downloaded
- **Multiple Models**: Supports various language models including Llama, Mistral, and others
- **Easy Setup**: Simple installation and model management

### Ollama API Endpoints Used:

- **`/api/tags`**: Lists all available models on the local Ollama instance
- **`/api/generate`**: Generates text responses using specified models

## Prerequisites

### 1. Install Ollama

Download and install Ollama from [https://ollama.ai](https://ollama.ai)

**Windows/Mac/Linux:**
```bash
# Visit https://ollama.ai and download the installer for your platform
```

### 2. Install the llama3.2 Model

After installing Ollama, download the required model:

```bash
ollama pull llama3.2
```

### 3. Start Ollama Service

Ensure Ollama is running on the default port:

```bash
ollama serve
```

The service should be accessible at `http://localhost:11434`

## Usage

1. **Open the Application**: Open `marketing_automation_ui.html` in your web browser
2. **Check Connection**: The app will automatically check if Ollama is running and if llama3.2 is available
3. **Input Business Details**: 
   - Business/Company Name
   - Target Customer Persona
   - Customer Challenges
   - Unique Selling Proposition (USP)
4. **Generate Workflow**: Click "Generate Workflow" to create your marketing automation strategy
5. **Review Results**: The AI-generated workflow will appear below the form

## Sample Data

The application comes pre-loaded with sample data for "TechFlow Solutions," a fictional marketing automation platform targeting SMB tech companies. This allows for immediate testing without manual data entry.

## Troubleshooting

### Common Issues:

**❌ Cannot connect to Ollama**
- Ensure Ollama is installed and running
- Check that the service is accessible at `http://localhost:11434`
- Verify firewall settings allow local connections

**⚠️ llama3.2 model not found**
- Run: `ollama pull llama3.2`
- Wait for the model download to complete
- Refresh the page to re-check model availability

**HTTP 404 Error**
- Verify Ollama service is running: `ollama serve`
- Check if the model name is correct in the API request
- Ensure no other applications are using port 11434

## Technical Details

### Model Configuration:
- **Model**: llama3.2
- **Temperature**: 0.7 (balanced creativity and consistency)
- **Top-p**: 0.9 (nucleus sampling for quality responses)
- **Max Tokens**: 2000 (sufficient for detailed workflows)

### Browser Compatibility:
- Modern browsers with ES6+ support
- Chrome, Firefox, Safari, Edge (latest versions)
- Requires JavaScript enabled

## File Structure

```
├── marketing_automation_ui.html    # Main application file
└── README.md                      # This documentation file
```

## Contributing

To modify or enhance the application:

1. Edit the HTML file to adjust the interface or functionality
2. Modify the JavaScript section to change AI model parameters
3. Update CSS styles for visual customization
4. Test thoroughly with your Ollama setup

## License

This project is open source and available for modification and distribution.

## Support

For issues related to:
- **Ollama**: Visit [Ollama Documentation](https://github.com/jmorganca/ollama)
- **This Application**: Check the troubleshooting section above or review the HTML source code

## Input Validation

The application includes comprehensive input validation and sanitization to ensure data quality and security:

### Validation Rules
- **Length Requirements**:
  - Minimum: 3 characters
  - Maximum: 500 characters per field

- **Allowed Characters**:
  - Letters (a-z, A-Z)
  - Numbers (0-9)
  - Spaces
  - Common punctuation (.,!?()-&+%'/)

### Security Features
- HTML tag stripping
- Special character escaping
- Real-time validation
- Form submission validation
- XSS prevention
- Input sanitization

### User Feedback
- Real-time validation on input blur
- Clear error messages
- Visual feedback for invalid inputs
- Summary of all errors on form submission

---

*Last Updated: 20240319*
