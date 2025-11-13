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

2. **Set up environment variables:**
   Create a `.env` file in the root directory with your Gemini API key:
   ```bash
   GEMINI_API_KEY=your_api_key_here
   ```
   > **Note:** The `.env` file is gitignored and will not be committed to version control.

3. **Install dependencies and build:**
   ```bash
   npm install
   npm run build
   ```
   This will generate `word-hover-extension/config.js` from your `.env` file.

4. **Open Chrome Extensions:**
   Navigate to `chrome://extensions` in your Chrome browser.

5. **Enable Developer Mode:**
   Turn on the "Developer mode" toggle, which is usually in the top-right corner.

6. **Load the Extension:**
   Click the "Load unpacked" button and select the `word-hover-extension` directory from the cloned repository.

The extension icon should now appear in your Chrome toolbar.

> **Important:** After making changes to `.env`, always run `npm run build` to regenerate `config.js` before reloading the extension.

## How to Use / 使い方

1. **Set Your Language / 言語を設定:**
   Click on the extension icon in your toolbar. Select your preferred target language from the dropdown and click "Save Language".

2. **Translate Words / 翻訳する:**
   Go to any webpage and hover your mouse over a word. A small tooltip will appear with the translation.

3. **Save Flashcards / 単語を保存:**
   In the translation tooltip, click the "Add" button to save the word and its translation to a flashcard deck.

4. **View Flashcards / フラッシュカードを見る:**
   Open the extension popup and navigate to the flashcards section to view your saved cards.

5. **Study / 学習:**
   Click on any flashcard to flip it over and see the translation. Click it again to see the original word. You can delete a card at any time using the "Delete" button.
