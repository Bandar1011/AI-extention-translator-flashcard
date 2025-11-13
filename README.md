# Hover Translator Chrome Extension / ホバー翻訳クローム拡張機能

EN: A simple Chrome extension that lets you hover over any word on a webpage to see its translation. You can also save words as two-sided flashcards to study later.

JP: ウェブページ上の単語にマウスをホバーすると、その場で翻訳が表示されるシンプルなChrome拡張機能です。さらに、単語を保存して「両面フラッシュカード」として学習できます。

## Features / 機能

🌐 **Instant Translation / 即時翻訳**
　カーソルを単語に重ねるだけで、ツールチップに翻訳が表示されます。

⚙️ **Customizable Language / 言語選択**
　拡張機能のポップアップから、好みのターゲット言語を選択できます。

🃏 **Flashcard System / フラッシュカード機能**
　気になる単語を保存し、自動で「表裏のあるフラッシュカード」に追加できます。

📖 **View & Manage Flashcards / フラッシュカード管理**
　保存したカードをポップアップで一覧表示し、クリックで裏返して暗記練習。覚えたカードは削除可能。

## Installation / インストール方法

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Bandar1011/hover-translator.git
   cd hover-translator
   ```

2. **Install dependencies and build (optional - for development only):**
   ```bash
   npm install
   npm run build
   ```
   > **Note:** The build step is optional. It generates `config.js` from `.env` for development convenience only. **No API keys are hardcoded in the extension** - users must provide their own.

3. **Open Chrome Extensions:**
   Navigate to `chrome://extensions` in your Chrome browser.

4. **Enable Developer Mode:**
   Turn on the "Developer mode" toggle, which is usually in the top-right corner.

5. **Load the Extension:**
   Click the "Load unpacked" button and select the `word-hover-extension` directory from the cloned repository.

6. **Configure Your API Key:**
   - Click the extension icon in your toolbar
   - Enter your Gemini API key in the settings (get one from [Google AI Studio](https://makersuite.google.com/app/apikey))
   - Select your target language
   - Click "Save Settings"

The extension icon should now appear in your Chrome toolbar.

> **Security Note:** This extension does NOT include any hardcoded API keys. Each user must provide their own Gemini API key via the extension settings. API keys are stored securely in Chrome's local storage (encrypted at rest) and never exposed in the extension bundle.

## How to Use / 使い方

1. **Configure API Key & Language / APIキーと言語を設定:**
   Click on the extension icon in your toolbar. Enter your Gemini API key (required) and select your preferred target language from the dropdown, then click "Save Settings".

2. **Translate Words / 翻訳する:**
   Go to any webpage and hover your mouse over a word. A small tooltip will appear with the translation.

3. **Save Flashcards / 単語を保存:**
   In the translation tooltip, click the "Add" button to save the word and its translation to a flashcard deck.

4. **View Flashcards / フラッシュカードを見る:**
   Open the extension popup and navigate to the flashcards section to view your saved cards.

5. **Study / 学習:**
   Click on any flashcard to flip it over and see the translation. Click it again to see the original word. You can delete a card at any time using the "Delete" button.
