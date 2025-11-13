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

**Quick Setup (3 steps):**

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Bandar1011/hover-translator.git
   cd hover-translator
   ```
   
   > **Note:** After cloning, you won't have `config.js` yet (it's gitignored). You'll create it in step 2.

2. **Add your API key and build:**
   
   Create a `.env` file in the root directory:
   ```bash
   echo "GEMINI_API_KEY=your_api_key_here" > .env
   ```
   
   Get your API key from [Google AI Studio](https://makersuite.google.com/app/apikey)
   
   Then build the extension:
   ```bash
   npm install
   npm run build
   ```
   
   This reads your `.env` file and **generates `config.js`** (which didn't exist before). The extension needs `config.js` to work.

3. **Load in Chrome:**
   - Open `chrome://extensions`
   - Enable "Developer mode" (top right)
   - Click "Load unpacked"
   - Select the `word-hover-extension` folder

**That's it!** The extension is ready to use. Just hover over words on any webpage to translate them.

> **Important:** Both `.env` and `config.js` are gitignored, so they stay local and won't be committed to git. Each user must create their own `.env` file and run `npm run build` to generate their own `config.js`.

## How to Use / 使い方

1. **Set Your Language (Optional):**
   Click on the extension icon in your toolbar and select your preferred target language from the dropdown, then click "Save Settings". Default is English.

2. **Translate Words / 翻訳する:**
   Go to any webpage and hover your mouse over a word. A small tooltip will appear with the translation.

3. **Save Flashcards / 単語を保存:**
   In the translation tooltip, click the "Add" button to save the word and its translation to a flashcard deck.

4. **View Flashcards / フラッシュカードを見る:**
   Open the extension popup and navigate to the flashcards section to view your saved cards.

5. **Study / 学習:**
   Click on any flashcard to flip it over and see the translation. Click it again to see the original word. You can delete a card at any time using the "Delete" button.
