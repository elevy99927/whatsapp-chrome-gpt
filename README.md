# ChatGPT Chrome Extension for WhatsApp Web

## Introduction

This Chrome extension integrates ChatGPT with WhatsApp Web, enabling users to generate AI-powered responses to messages. With features like message retrieval, interaction with OpenAI's API, and seamless copy-paste functionality, this extension enhances messaging efficiency.

## Key Features

- **Integration with ChatGPT:** Send messages to OpenAI's GPT and receive intelligent responses.
- **Copy and Paste:** Easily copy responses or paste them directly into the chat.
- **Floating UI:** Access and interact with the extension through an intuitive floating button on WhatsApp Web.

## Prerequisites

- A valid OpenAI API key (<a href='https://platform.openai.com/'>https://platform.openai.com</a>).
- Google Chrome browser.
- Basic knowledge with <a href='https://support.google.com/chrome_webstore/answer/2664769?hl=en'>install and manage chrome extensions</a>.


## Installation Instructions

1. **Download or Clone the Repository:**

   ```bash
   git clone https://github.com/elevy99927/whatsapp-chrome-gpt.git
   ```

2. **Add the API Key:**

   - Open the `config.json` file.
   - Add your OpenAI API key under `OPENAI_API_KEY`.

3. **Load the Extension in Chrome:**

   - Go to `chrome://extensions`.
   - Enable **Developer mode**.
   - Click **Load unpacked** and select the project folder.

4. **Reload WhatsApp Web:**

   - Open `https://web.whatsapp.com` in Chrome.
   - Ensure the floating button appears on the interface.

## Configuration

The `config.json` file is used to configure the extension. Add your OpenAI API key as follows:

```json
{
  "OPENAI_API_KEY": "your-openai-api-key"
}
```

## How It Works

1. **Activate the Extension:**
   - Click the floating "Send to GPT" button.
2. **Retrieve the Last Message:**
   - The extension fetches the last message from the active chat.
3. **Send Message to ChatGPT:**
   - The message is sent to OpenAI's API, and a response is generated.
4. **Display and Interact with Response:**
   - The response is displayed in a floating window with "Copy" and "Paste" options.

## Permissions Required

- **Active Tab:** To interact with WhatsApp Web's DOM.
- **Storage:** To store the API key.
- **Clipboard Access:** For copy-paste functionality.

## Project Structure

- **`background.js`:** Handles communication with OpenAI's API and manages the core logic of the extension.
- **`content.js`:** Manages DOM interaction, displays the floating UI, and handles user interactions like sending and receiving messages.
- **`manifest.json`:** Defines the extension's metadata, permissions, and configuration.
- **`config.json`:** Stores the OpenAI API key and optional configuration like language preferences.

## Additional Features

### Minimize and Interaction Buttons
- The floating UI includes "Minimize" and "Copy" buttons for convenient interaction with responses.
- Responses can be copied directly to the clipboard or pasted into the WhatsApp chat input.

### Debugging
- A debug mode can be enabled by setting `debug` to `true` in the `background.js` file to help identify and resolve issues.

### Mermaid Diagram
Below is a high-level architecture of the extension:

```mermaid
graph LR
A[WhatsApp Web] --> B[content.js: Fetch Messages]
B --> C[background.js: Send to OpenAI API]
C --> D[OpenAI API]
D --> C
C --> B
B --> E[UI: Display Response]
E --> F[User Interaction: Copy/Paste]
```

## Troubleshooting

- **Extension Context Invalidated:** Reload the extension and refresh WhatsApp Web.
- **API Errors:** Verify your OpenAI API key and ensure it has the required permissions.
- **Floating Button Missing:** Ensure the extension is loaded correctly and refresh the page.

## Limitations

- Only compatible with WhatsApp Web.
- Relies on OpenAI's API availability.

## Future Enhancements

- Support for additional messaging platforms.
- Enhanced UI with customization options.
- Multi-language support for a broader audience.

## Acknowledgments

- **OpenAI:** For providing the ChatGPT API.
- **Chrome Extension APIs:** For enabling seamless integration.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Additional Credits

This project was inspired and developed with contributions from various open-source communities and tools. Special thanks to all contributors for their support and ideas.

## Contact

For questions or feedback, feel free to reach out:

- **Email**: eyal@levys.co.il
- **GitHub**: [https://github.com/elevy99927](https://github.com/elevy99927)

