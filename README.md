# SQoogLe

SQoogLe is a beginner-friendly SQL Query Explainer. You paste SQL, click a button, and it explains each line in simple English.

## What this project does

- Takes your SQL query from a text box.
- Sends it to OpenAI using your API key.
- Gets back line-by-line explanations.
- Shows the explanation in a chat-style interface.

## File in this project

- `index.html`: full app (HTML + CSS + JavaScript in one file).

## Run on your MacBook Air (Step-by-step)

### Option A: Quickest way (double-click)

1. Open Finder.
2. Go to this folder: `SQoogLe`.
3. Double-click `index.html`.
4. It opens in your browser.

### Option B: Using VS Code + Live Server (recommended)

1. Open folder in VS Code.
2. Install extension **Live Server** (by Ritwick Dey).
3. Right-click `index.html` and click **Open with Live Server**.
4. Browser opens with a local URL.

## How to use

1. Paste your OpenAI API key into **OpenAI API key**.
2. Keep model as `gpt-4.1-mini` (or replace with another available model from your trainer).
3. Paste SQL query in the SQL box.
4. Click **Explain Query**.
5. Read summary + line-by-line explanation in chat.

Shortcut: press `Cmd + Enter` in the SQL box to run quickly.

## Important security note (very important)

For learning, entering API key in frontend is okay.
For real/production apps, never expose API keys in browser code. Use a backend server to call OpenAI securely.

## How the code works (simple explanation)

1. HTML creates inputs and chat layout.
2. CSS styles everything (colors, cards, chat bubbles).
3. JavaScript does this flow:
	- reads your SQL and key
	- sends request to `https://api.openai.com/v1/chat/completions`
	- asks model to return JSON with summary + per-line explanation
	- parses JSON and displays it nicely

## If you get errors

- `Missing API key`: add your key.
- `OpenAI API error 401`: invalid key or expired key.
- `OpenAI API error 429`: rate limit/quota exceeded.
- Model error (`404` or similar): model name not available for your key. Try a different model.

## Next learning step

After this works, a great next step is splitting `index.html` into:

- `index.html`
- `style.css`
- `app.js`

This helps you learn clean project structure.
