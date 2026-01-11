# Automation Practice Ground

**Automation Practice Ground** is a comprehensive web testing playground designed for practicing test automation. Whether you are using **Selenium**, **Playwright**, **Cypress**, or any other test automation tool, this project provides a diverse set of scenarios to hone your skills.

Inspired by the classic *the-internet*, Automation Practice Ground brings a modern aesthetic using vanilla HTML, CSS, and JavaScript, ensuring a fast, lightweight, and stable environment for your tests.

## 🚀 Features

*   **40+ Interactive Scenarios**: Covering everything from basic inputs to complex Shadow DOM interactions.
*   **Zero Dependencies**: Built with pure HTML5, CSS3, and JavaScript. No complex build steps or frameworks.
*   **Modern Design**: Clean UI with responsive layouts, making visual regression testing more interesting.
*   **Stable Selectors**: Designed to be automatable, but with intentional challenges (e.g., dynamic IDs, shifting content).
*   **Real-world Edge Cases**: Simulates common web issues like slow network resources, broken images, and authentication popups.

## 📂 Available Scenarios

The project includes a wide variety of practice pages:

### 🔹 Basic Interaction
*   **[A/B Testing](pages/ab-testing.html)**: Testing varied content.
*   **[Add/Remove Elements](pages/add-remove-elements.html)**: Handling dynamic DOM elements.
*   **[Checkboxes](pages/checkboxes.html)** & **[Inputs](pages/inputs.html)**: Standard form controls.
*   **[Dropdown](pages/dropdown.html)**: Standard and Searchable dropdowns.
*   **[Key Presses](pages/key-presses.html)**: Keyboard event handling.
*   **[Typos](pages/typos.html)**: Text validation practice.

### 🔹 Intermediate Interaction
*   **[Context Menu](pages/context-menu.html)**: Right-click interactions.
*   **[Drag and Drop](pages/drag-and-drop.html)**: HTML5 drag and drop events.
*   **[Hovers](pages/hovers.html)**: Mouse hover states.
*   **[Horizontal Slider](pages/horizontal-slider.html)**: Range input manipulation.
*   **[Multiple Windows](pages/multiple-windows.html)**: Handling browser tabs/windows.
*   **[Frames](pages/frames.html)**: Nested frames and iFrames.
*   **[JavaScript Alerts](pages/javascript-alerts.html)**: Handling native browser alerts/prompts.
*   **[File Download & Upload](pages/file-download-upload.html)**: File system interactions.

### 🔹 Advanced & Dynamic Content
*   **[Challenging DOM](pages/challenging-dom.html)**: Hard-to-select elements with dynamic properties.
*   **[Dynamic Loading](pages/dynamic-loading.html)**: Handling asynchronous content (AJAX).
*   **[Dynamic Controls](pages/dynamic-controls.html)**: Elements enabling/disabling or appearing/disappearing.
*   **[Shadow DOM](pages/shadow-dom.html)**: Automating within Shadow Roots.
*   **[Infinite Scroll](pages/infinite-scroll.html)**: Scroll-based data loading.
*   **[Slow Resources](pages/slow-resources.html)**: Simulating network latency.
*   **[Advanced XPath: SVG](pages/svg-xpath.html)**: Working with SVG elements and graphs.

### 🔐 Authentication & Security
*   **[Basic Auth](pages/basic-auth.html)**: Native browser basic authentication.
*   **[Digest Auth](pages/digest-auth.html)**: Native browser digest authentication.
*   **[Form Authentication](pages/form-auth.html)**: Standard login form.
*   **[Forgot Password](pages/forgot-password.html)**: Password recovery flow.

*(See the full list in the `pages/` directory or on the homepage)*

## 🛠️ Getting Started

Since this project uses vanilla web technologies, you can run it easily without a heavy backend.

### Option 1: Open Directly
Simply double-click `index.html` to open it in your default browser.
*Note: Some features like "Copy to Clipboard" or Authentication popups might behave differently via `file://` protocol.*

### Option 2: Run a Local Server (Recommended)
For the best experience, run it using a simple HTTP server.

**Using Python:**
```bash
# Python 3
python -m http.server 8000
```

Notes: 
depending on your python version / installation, you might need to use `python3` instead of `python`.

**Using Node.js (npx):**
```bash
npx serve .
```
Notes:
depending on your existing configuration, you might need to use `npx serve . --port 8000` instead, or your prefered port if the port already in use.

Then visit `http://localhost:8000` (or the port shown in your terminal).

## 🤝 Contributing

Feel free to fork this project and add more scenarios! If you find a bug or think of a new automation challenge, please open an issue or submit a PR.

## 📝 License

This project is free to use for educational purposes.

I'm currently very active in exploring AI utilization for testing apps and software development purpose. If you want to buy me a coffee or support me with software licenses (e.g. Google AI Pro/Ultra, Github Copilot, Claude, etc), reach out to me here: <a href="https://sociabuzz.com/farizagati">Fariz Agati</a>

Happy Testing!
