<p align="center">
  <img src="./img.png" alt="GlowWise Banner" width="100%">
</p>

# GlowWise 🎯

GlowWise is a single-page, client-side web application that generates personalized skincare product recommendations based on user input (skin type, concerns, allergies, budget). This repository contains the frontend demo built with vanilla HTML, CSS and JavaScript.

## Team

- **Team name:** byTheBie
- **Members:** Diya, Chintu (Toch Institute of Science And Technology)

## Live demo

https://glow-wise.vercel.app/

## Repository structure

- `frontend/`
  - `index.html` — app shell and page container
  - `assets/css/style.css` — extracted stylesheet
  - `assets/js/script.js` — main application logic, sample product & category data

Open the `frontend/` folder to run a local copy.

## Key features

- Guided quiz and tag inputs to capture skin type, concerns, and allergies
- Client-side product DB with compatibility scoring and sample reviews
- Results grid, product detail view, save/favourites, and review posting (stored in LocalStorage)
- LocalStorage persistence for users, search history and saved products

## Recent changes / important notes

- The original project was a single HTML file with embedded CSS/JS. It has been refactored so styles and scripts live in `assets/css/style.css` and `assets/js/script.js`.
- A temporary corruption was found in `index.html` during the split; the file was replaced with a minimal shell that includes the DOM element IDs the script expects. If you need the original full UI markup restored, I can re-insert it from the original source.

## Run locally (quick)

1. Open a terminal in the `frontend` folder.
2. Start a static server (Python 3):

```powershell
python -m http.server 8000
```

3. Open http://127.0.0.1:8000/ in a browser (or use the VS Code Simple Browser).

Notes:
- The app is client-only; no backend is required.
- If you prefer Node, use `npx http-server . -p 8000` from the `frontend` folder.

## Troubleshooting

- Blank page or JS errors: open the browser console (F12) and check error messages.
- Common fixes:
  - Ensure `assets/js/script.js` is present and included only once in `index.html`.
  - Ensure `index.html` contains the DOM IDs used by the script (`summaryBanner`, `resultGrid`, `detail-content`, `sidePanel`, `sideOverlay`, `filterPanel`, `userChip`, etc.).
  - Clear app state: DevTools → Application → LocalStorage → remove `gw_users` and any `gw_data_*` entries.
- If a function is undefined, verify `assets/js/script.js` is not truncated and is loaded after the DOM elements it references.

## Development notes

- The sample product and category data live inside `assets/js/script.js` for demo simplicity.
- The app uses inline event attributes in HTML (e.g., `onclick="openSidePanel()"`); when renaming functions, update both the HTML and the script.

## Testing flows

- Complete the quiz → select budget → start analysis → view results grid
- Open a product card → save to favourites → open profile to view saved items
- Sign up / Sign in (data saved in LocalStorage) or continue as guest

## Contributing

- Make changes in the `frontend/` folder. If you change DOM IDs or function names, update `assets/js/script.js` accordingly.
- Open a pull request describing your change and the steps to verify it.

## AI tools & acknowledgements

- Tools used during development: GitHub Copilot, ChatGPT (for guidance), Claude (optional).
- Human contributions: UI/UX design, product data curation, application logic and testing.

## License

This project is released under the MIT License — see the full text below.

---

Copyright (c) 2026 byTheBie

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

```

#### Demo Output

**Example 1: Basic Processing**

**Input:**
```
This is a sample input file
with multiple lines of text
for demonstration purposes
```

**Command:**
```bash
python script.py sample.txt
```

**Output:**
```
Processing: sample.txt
Lines processed: 3
Characters counted: 86
Status: Success
Output saved to: output.txt
```

**Example 2: Advanced Usage**

**Input:**
```json
{
  "name": "test",
  "value": 123
}
```

**Command:**
```bash
python script.py -v --format json data.json
```

**Output:**
```
[VERBOSE] Loading configuration...
[VERBOSE] Parsing JSON input...
[VERBOSE] Processing data...
{
  "status": "success",
  "processed": true,
  "result": {
    "name": "test",
    "value": 123,
    "timestamp": "2024-02-07T10:30:00"
  }
}
[VERBOSE] Operation completed in 0.23s
```

---

## Project Demo

### Photo
https://drive.google.com/drive/folders/14JI2f7BxntCG9-cHyPT0T-bz9L7MfzMn?usp=drive_link

### Video
https://drive.google.com/file/d/1gl2uPiZNtQ5EJQSeZZ8TZj8bjmuQyg7i/view?usp=sharing



## AI Tools Used (Optional - For Transparency Bonus)


**Tool Used:** [ GitHub Copilot, ChatGPT, Claude]


**Key Prompts Used:**
- "Create a REST API endpoint for user authentication"
- "Debug this async function that's causing race conditions"
- "Optimize this database query for better performance"

**Percentage of AI-generated code:** [Approximately X%]

**Human Contributions:**
- Architecture design and planning
- Custom business logic implementation
- Integration and testing
- UI/UX design decisions

*Note: Proper documentation of AI usage demonstrates transparency and earns bonus points in evaluation!*

---

## Team Contributions

- [Name 1]: [Specific contributions - e.g., Frontend development, API integration, etc.]
- [Name 2]: [Specific contributions - e.g., Backend development, Database design, etc.]
- [Name 3]: [Specific contributions - e.g., UI/UX design, Testing, Documentation, etc.]

---

## License

This project is licensed under the [LICENSE_NAME] License - see the [LICENSE](LICENSE) file for details.

**Common License Options:**
- MIT License (Permissive, widely used)
- Apache 2.0 (Permissive with patent grant)
- GPL v3 (Copyleft, requires derivative works to be open source)

---

Made with ❤️ at TinkerHub
