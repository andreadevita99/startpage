# 🖥️ Terminal-inspired Brave Startpage

A terminal-inspired startpage for **Brave** (and other Chromium-based browsers).<br>
Developed entirely in a **single HTML file** using pure HTML, CSS, and vanilla JavaScript, with no external dependencies or frameworks.

## ✨ Features

- **Modern Terminal Interface:** Clean design, smooth animations, and support for polished visual effects.
- **Single File:** Everything (HTML, CSS, JS) lives in a single `index.html` file. Zero dependencies, zero build step.
- **Multiple Themes:** Choose from 6 themes (Dark, Light, Nord, Gruvbox, Tokyo Night, Catppuccin).
- **Integrated Weather:** Minimalist always-visible widget and `weather` command with 5-day forecast (powered by Open-Meteo).
- **Temperature Units:** Support for Celsius (°C), Fahrenheit (°F), and Kelvin (K).
- **Search Engines:** Brave by default, but also supports Google, Qwant, DuckDuckGo, Ecosia, and Startpage.
- **Personal Notes:** Save, search, and manage quick notes directly from the terminal (saved in `localStorage`).
- **Calendar and Countdown:** Display the current month in ASCII art and calculate days remaining until a date.
- **Smart Autocomplete:** Dropdown for commands and arguments with fuzzy matching (Levenshtein).
- **Internationalization (i18n):** Fully bilingual interface (Italian/English) with an iOS-style toggle.
- **Useful Commands:** `calc`, `ping`, `ip`, `neofetch`, `man`, `llm` (for Ollama), `ask` (Brave AI).
- **Persistence:** Command history, notes, settings, and preferences saved locally. Support for Config Export/Import.

## 🚀 How to Install on Brave

Since Brave does not allow you to replace the "New Tab" page with a local file directly from the settings, you have two options:

### Method 1: Startup Page (Recommended)

1. Save the code in a file named `index.html` (e.g., in your Documents folder).
2. Open Brave and drag the `index.html` file into a new tab to get the path (e.g., `file:///C:/Users/Name/Documents/index.html`). Copy it.
3. Go to `brave://settings/getStarted`.
4. Select **"Open a specific page or set of pages"**.
5. Click **"Add a new page"** and paste the copied path.

### Method 2: Replace the "New Tab" (Requires Extension)

1. Install an extension that replaces the "New Tab" default window from the Chrome Web Store.
2. Configure the extension by pasting the `file:///...` path to your HTML file.

> ⚠️ **Note for Linux users:** If you use Brave via Snap or Flatpak, the browser is sandboxed and may not read local files. In this case, use the `.deb` package or a new tab extension.

## ⌨️ Available Commands

Type `help` to display the full list. Here are the main ones:

| Command                   | Description                                 | Example                           |
| :------------------------ | :------------------------------------------ | :-------------------------------- |
| `s <query>`               | Search using the default engine             | `s how to learn javascript`       |
| `weather [city]`          | Show weather (default: Rome or geolocation) | `weather Milan --days=7 --unit=f` |
| `calendar [month] [year]` | Display monthly ASCII calendar              | `calendar 12 2026`                |
| `notes <add/list/rm>`     | Manage personal notes                       | `notes add Buy milk`              |
| `engine <name>`           | Change search engine                        | `engine duckduckgo`               |
| `theme <name>`            | Change visual theme                         | `theme tokyo-night`               |
| `unit <c/f/k>`            | Change temperature unit                     | `unit f`                          |
| `lang <it/en>`            | Change interface language                   | `lang en`                         |
| `calc <expression>`       | Safe calculator                             | `calc (15 * 4) / 2`               |
| `config <export/import>`  | Export or import settings                   | `config export`                   |
| `neofetch`                | Show system and browser info                | `neofetch`                        |
| `llm <prompt>`            | Send a prompt to local Ollama (if running)  | `llm explain relativity`          |

## ⌨️ Keyboard Shortcuts

| Key              | Action                                      |
| :--------------- | :------------------------------------------ |
| `Tab`            | Autocomplete commands and arguments         |
| `↑` / `↓`        | Navigate history or suggestions dropdown    |
| `Ctrl + L`       | Clear screen (like `clear`)                 |
| `Ctrl + U`       | Clear current input line                    |
| `Ctrl + W`       | Delete last typed word                      |
| `Ctrl + C`       | Cancel fetch (e.g., weather) or clear input |
| `Esc`            | Clear input and close menus                 |
| `Click` Clock    | Toggle 12h / 24h format                     |
| `Click` Weather  | Force weather refresh                       |
| `Click` Language | Toggle IT / EN                              |

## ⚙️ Configuration and URL Parameters

You can force specific settings by passing parameters in the URL (useful if you host it on a server):

- `?theme=nord` (Set theme)
- `?user=Marco` (Set username for greeting)
- `?city=Tokyo` (Set default city for weather)
- `?unit=f` (Set Fahrenheit by default)
- `?lang=en` (Set English language)
- `?engine=qwant` (Set Qwant as search engine)
- `?clock=12` (Set clock to 12 hours)

## 🛠️ Tech Stack

- **HTML5 / CSS3 / JavaScript (ES6+)**
- **Open-Meteo API:** For weather data and geocoding (free, no API key).
- **LocalStorage:** To persist notes, themes, history, and preferences.
- **Ollama (Optional):** If running on `localhost:11434`, enables the `llm` command for local AI.

## Author

[Andrea De Vita](https://github.com/andreadevita99)

## License

All rights reserved. This project is provided for demonstration purposes only. No permission is granted to use, copy, modify, merge, publish, distribute, sublicense, or otherwise reproduce any part of this software without explicit written consent from the author. Unauthorized use, modification, or redistribution is strictly prohibited.
