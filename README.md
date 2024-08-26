# Chatbot-Integration-with-HTML
Certainly! Let's go through the code section by section, explaining its purpose and functionality.

### 1. **HTML Document Structure**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wi-Five Help</title>
```

- **`<!DOCTYPE html>`**: This declaration defines the document as an HTML5 document.
- **`<html lang="en">`**: The `<html>` tag is the root element of the HTML document. The `lang` attribute specifies the language of the document (English).
- **`<head>`**: The head section contains meta-information about the document, such as the character encoding (`UTF-8`), viewport settings for responsive design, and the title of the page, which will be displayed in the browser tab.

### 2. **CSS Styling**

```html
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #000;
            color: #fff;
            margin: 0;
            padding: 0;
        }
```

- **`body`**: 
  - **`font-family: Arial, sans-serif;`**: Sets the font for the entire document to Arial, with sans-serif as a fallback.
  - **`background-color: #000;`**: Sets the background color to black.
  - **`color: #fff;`**: Sets the text color to white.
  - **`margin: 0; padding: 0;`**: Removes default margin and padding to ensure the content aligns properly with the edges of the browser window.

```html
        header {
            background-color: #ff0000;
            padding: 10px 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
```

- **`header`**: 
  - **`background-color: #ff0000;`**: Sets the background color of the header to red.
  - **`padding: 10px 20px;`**: Adds padding inside the header for spacing.
  - **`display: flex;`**: Applies flexbox layout to the header, which helps in aligning the content.
  - **`justify-content: space-between;`**: Distributes space between the logo and navigation links, pushing them to opposite ends.
  - **`align-items: center;`**: Vertically centers the logo and navigation links within the header.

```html
        nav a {
            color: #fff;
            text-decoration: none;
            margin: 0 15px;
        }
        nav a:hover {
            text-decoration: underline;
        }
```

- **`nav a`**: 
  - **`color: #fff;`**: Sets the color of the navigation links to white.
  - **`text-decoration: none;`**: Removes the default underline from the links.
  - **`margin: 0 15px;`**: Adds horizontal space between each link.
  
- **`nav a:hover`**: 
  - **`text-decoration: underline;`**: Adds an underline to the links when hovered over.

```html
        .content-container {
            display: flex;
            justify-content: space-between;
            padding: 20px;
        }
```

- **`.content-container`**: 
  - **`display: flex;`**: Uses flexbox to align its child elements (customer care and chatbot sections).
  - **`justify-content: space-between;`**: Spaces the child elements evenly.
  - **`padding: 20px;`**: Adds padding around the content.

```html
        .customer-care-container, .chatbot-container {
            background-color: #8B0000;
            border-radius: 15px;
            padding: 20px;
            width: 45%;
        }
```

- **`.customer-care-container, .chatbot-container`**: 
  - **`background-color: #8B0000;`**: Sets the background color to dark red.
  - **`border-radius: 15px;`**: Rounds the corners of the containers.
  - **`padding: 20px;`**: Adds space inside the containers.
  - **`width: 45%;`**: Each container takes up 45% of the available width, with space between them.

```html
        .chat-log {
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid #ddd;
            padding: 10px;
            background-color: #fff;
            color: #000;
            margin-bottom: 10px;
        }
```

- **`.chat-log`**: 
  - **`max-height: 300px;`**: Limits the height of the chat log to 300px.
  - **`overflow-y: auto;`**: Adds a vertical scrollbar if the content exceeds 300px.
  - **`border: 1px solid #ddd;`**: Adds a light gray border.
  - **`padding: 10px;`**: Adds padding inside the chat log.
  - **`background-color: #fff;`**: Sets the background color to white.
  - **`color: #000;`**: Sets the text color to black.
  - **`margin-bottom: 10px;`**: Adds space below the chat log.

```html
        .input-container input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }
```

- **`.input-container input`**: 
  - **`flex: 1;`**: Makes the input field expand to fill available space within its container.
  - **`padding: 10px;`**: Adds padding inside the input field.
  - **`border: 1px solid #ddd;`**: Adds a light gray border.
  - **`border-radius: 5px;`**: Rounds the corners of the input field.

```html
        .input-container button {
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            background-color: #674188;
            color: #fff;
            cursor: pointer;
        }
```

- **`.input-container button`**: 
  - **`padding: 10px;`**: Adds padding inside the button.
  - **`border: 1px solid #ddd;`**: Adds a light gray border.
  - **`border-radius: 5px;`**: Rounds the corners of the button.
  - **`background-color: #674188;`**: Sets the background color to a purple shade.
  - **`color: #fff;`**: Sets the text color to white.
  - **`cursor: pointer;`**: Changes the cursor to a pointer when hovering over the button.

```html
        .button {
            margin: 5px 0;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            color: #fff;
            cursor: pointer;
        }
```

- **`.button`**: 
  - **`margin: 5px 0;`**: Adds vertical spacing above and below the button.
  - **`padding: 10px;`**: Adds padding inside the button.
  - **`border: 1px solid #ddd;`**: Adds a light gray border.
  - **`border-radius: 5px;`**: Rounds the corners of the button.
  - **`color: #fff;`**: Sets the text color to white.
  - **`cursor: pointer;`**: Changes the cursor to a pointer when hovering over the button.

```html
        .back-button {
            background-color: #508C9B;
        }
        .issue-button {
            background-color: #FF6F61;
        }
        .resolve-button {
            background-color: #4CAF50;
        }
        .resolve-button-no {
            background-color: #FF5722;
        }
        .resolve-options {
            display: flex;
            justify-content: space-between;
        }
    </style>
</head>
```

- **`.back-button`**: 
  - Sets the background color to teal.
  
- **`.issue-button`**: 
  - Sets the background color to a coral shade.
  
- **`.resolve-button`**: 
  - Sets the background color to green.
  
- **`.resolve-button-no`**: 
  - Sets the background color to orange.
  
- **`.resolve-options`**: 
  - Uses flexbox to arrange the resolution buttons side by side.

### 3. **Body Content**

```html
<body>
<header>
    <img src="dependencies/logo.png" alt="Wi-Five Logo">
    <nav>
        <a href="myaccount.html">My Account</a>
        <a href="plandetails.html">Plan Details</a>
        <a href="products.html">Products</a>
        <a href="help.html">Help</a>
    </nav>
</header>
```

- **`<header>`**: 
  - Contains the company logo and navigation links to other parts of the website, such as "My Account," "Plan Details

," "Products," and "Help."

```html
<div class="content-container">
    <div class="customer-care-container">
        <h2>Customer Care</h2>
        <p><strong>Call Us:</strong> <a href="tel:+911234567890">+91-1234567890</a></p>
        <p><strong>Email Us:</strong> <a href="mailto:wifive12345@gmail.com">wifive12345@gmail.com</a></p>
    </div>
    <div class="chatbot-container">
        <h2>Chat with Us</h2>
        <div id="chat-log" class="chat-log"></div>
        <div class="input-container">
            <button id="backButton" class="back-button" onclick="goBack()">Back</button>
            <button id="issueButton" class="issue-button" onclick="displayIssueButtons()">Choose Issue</button>
        </div>
    </div>
</div>
```

- **`<div class="content-container">`**: 
  - A flexbox container holding two main sections: Customer Care and Chatbot.
  
- **`<div class="customer-care-container">`**: 
  - Displays customer care contact information, including a phone number and email address.
  
- **`<div class="chatbot-container">`**: 
  - Houses the chatbot interface with a chat log and buttons for interacting with the chatbot.

### 4. **JavaScript Functionality**

```html
<script>
    const intents = {
        "network_issue": {
            "patterns": ["My internet is slow", "No connection", "Network down", "Wifi not working"],
            "responses": ["Please restart your router.", "Is the network cable connected properly?", "Try resetting your modem.", "Check if the service is down in your area."]
        },
        "vpn_issue": {
            "patterns": ["VPN not connecting", "Unable to connect to VPN", "VPN is slow"],
            "responses": ["Please check your VPN settings.", "Restart your device and try again.", "Is your internet connection stable?"]
        }
        // Add more issues and patterns/responses as needed
    };
```

- **`intents` Object**: 
  - Stores different issues (e.g., "network_issue", "vpn_issue") with associated patterns (user input examples) and responses (chatbot replies).
  
```html
    function displayIssueButtons() {
        const chatLog = document.getElementById("chat-log");
        chatLog.innerHTML = "";
        for (const intent in intents) {
            const button = document.createElement("button");
            button.classList.add("button", "issue-button");
            button.textContent = intent.replace("_", " ").toUpperCase();
            button.onclick = () => showPatterns(intent);
            chatLog.appendChild(button);
        }
    }
```

- **`displayIssueButtons()`**: 
  - Clears the chat log and creates buttons for each issue defined in the `intents` object. When a button is clicked, it calls `showPatterns(intent)`.

```html
    function showPatterns(tag) {
        const chatLog = document.getElementById("chat-log");
        chatLog.innerHTML = `<p>Choose a related query:</p>`;
        intents[tag].patterns.forEach(pattern => {
            const patternButton = document.createElement("button");
            patternButton.classList.add("button");
            patternButton.textContent = pattern;
            patternButton.onclick = () => sendMessage(pattern);
            chatLog.appendChild(patternButton);
        });
        const backButton = document.createElement("button");
        backButton.textContent = "Back";
        backButton.classList.add("button", "back-button");
        backButton.onclick = () => displayIssueButtons();
        chatLog.appendChild(backButton);
    }
```

- **`showPatterns(tag)`**: 
  - Displays buttons for each pattern related to the selected issue. Clicking a pattern sends the message to the chatbot using `sendMessage(pattern)`.

```html
    function goBack() {
        displayIssueButtons();
    }
```

- **`goBack()`**: 
  - Calls `displayIssueButtons()` to return to the main issue selection screen.

```html
    function sendMessage(message) {
        const chatLog = document.getElementById("chat-log");
        const userMessage = document.createElement("p");
        userMessage.textContent = "You: " + message;
        chatLog.appendChild(userMessage);
        const botResponse = document.createElement("p");
        botResponse.textContent = "Wi-Five Bot: " + getResponse(message);
        chatLog.appendChild(botResponse);
        chatLog.scrollTop = chatLog.scrollHeight;
        setTimeout(() => {
            displayResolveOptions();
        }, 500);
    }
```

- **`sendMessage(message)`**: 
  - Displays the user's message and the chatbot's response in the chat log. After a short delay, it shows the resolution options.

```html
    function getResponse(message) {
        for (const intent in intents) {
            for (const pattern of intents[intent].patterns) {
                if (message.toLowerCase() === pattern.toLowerCase()) {
                    const responses = intents[intent].responses;
                    return responses[Math.floor(Math.random() * responses.length)];
                }
            }
        }
        return "I'm sorry, I didn't understand that. Please contact customer care.";
    }
```

- **`getResponse(message)`**: 
  - Searches for the user's message in the patterns of the intents. If found, it returns a random response from the corresponding intent. If not, it returns a generic error message.

```html
    function displayResolveOptions() {
        const chatLog = document.getElementById("chat-log");
        const resolveOptions = document.createElement("div");
        resolveOptions.classList.add("resolve-options");
        const resolveYes = document.createElement("button");
        resolveYes.textContent = "Yes";
        resolveYes.classList.add("button", "resolve-button");
        resolveYes.onclick = () => issueResolved(true);
        resolveOptions.appendChild(resolveYes);
        const resolveNo = document.createElement("button");
        resolveNo.textContent = "No";
        resolveNo.classList.add("button", "resolve-button-no");
        resolveNo.onclick = () => issueResolved(false);
        resolveOptions.appendChild(resolveNo);
        chatLog.appendChild(resolveOptions);
    }
```

- **`displayResolveOptions()`**: 
  - Creates "Yes" and "No" buttons asking if the issue was resolved. The buttons call `issueResolved(true)` or `issueResolved(false)`.

```html
    function issueResolved(resolved) {
        const chatLog = document.getElementById("chat-log");
        const resolveMessage = document.createElement("p");
        if (resolved) {
            resolveMessage.textContent = "Wi-Five Bot: Glad I could help!";
        } else {
            resolveMessage.textContent = "Wi-Five Bot: Please contact customer care for further assistance.";
        }
        chatLog.appendChild(resolveMessage);
        setTimeout(() => {
            displayIssueButtons();
        }, 1000);
    }
    displayIssueButtons();
</script>
```

- **`issueResolved(resolved)`**: 
  - Displays a message based on whether the issue was resolved. After a delay, it returns to the main issue selection screen.

- **`displayIssueButtons()`**: 
  - Automatically runs when the page loads to display the initial set of issue buttons.

### 5. **Closing Tags**

```html
</body>
</html>
```

- **`</body>`**: Closes the body section of the document.
- **`</html>`**: Closes the HTML document.

---

This code creates a webpage with a help and support section, including a chatbot that helps users troubleshoot common issues by selecting problems, sending messages, and receiving automated responses. The design is responsive and user-friendly, with a modern interface consistent with the Wi-Five brand.
