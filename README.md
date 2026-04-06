# SQoogLe

SQoogLe is a beginner-friendly SQL Query Explainer. You paste SQL, click a button, and it explains each line in simple English.

## What this project does

- Takes your SQL query from a text box.
- Sends it to OpenAI using your API key.
- Gets back line-by-line explanations.
- Shows the explanation in a chat-style interface.

## File in this project

- `index.html`: full app (HTML + CSS + JavaScript in one file).

## Run on your MacBook Air

### Option A: Quickest way

1. Open Finder.
2. Go to the `SQoogLe` folder.
3. Double-click `index.html`.
4. It opens in your browser.

### Option B: Using VS Code + Live Server

1. Open the folder in VS Code.
2. Install the **Live Server** extension.
3. Right-click `index.html`.
4. Click **Open with Live Server**.

## How to use

1. Paste your OpenAI API key into **OpenAI API key**.
2. Keep model as `gpt-4.1-mini` or replace it with a model name available on your account.
3. Paste SQL query in the SQL box.
4. Click **Explain Query**.
5. Read the summary and line-by-line explanation in the chat area.

Shortcut: press `Cmd + Enter` in the SQL box to run quickly.

## Important security note

For learning, entering API key in frontend is okay.
For real apps, never expose API keys in browser code. Use a backend server to call OpenAI securely.

## How the code works

1. HTML creates the layout and form fields.
2. CSS styles the page.
3. JavaScript reads your SQL and API key.
4. JavaScript sends a request to `https://api.openai.com/v1/chat/completions`.
5. The model returns JSON with a summary and per-line explanation.
6. The page displays the result in chat format.

## If you get errors

- `Missing API key`: add your key.
- `OpenAI API error 401`: key is invalid or expired.
- `OpenAI API error 429`: rate limit or quota exceeded.
- `404` model error: model name may not be available for your key.
