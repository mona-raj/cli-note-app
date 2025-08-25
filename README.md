# CLI Note App 📝

A simple **command-line based note-taking app** built with **Node.js**.
Notes are stored in a **JSON file** and can be managed using a clean **CLI interface powered by [yargs](https://www.npmjs.com/package/yargs)**.
The app also comes with a lightweight **web view** to browse notes in the browser.

🔗 GitHub Repository: [mona-raj/cli-note-app](https://github.com/mona-raj/cli-note-app/tree/main)

---

## ✨ Features

* Create, list, search, and delete notes from the terminal.
* Launch a local web server to view notes in the browser.
* Notes stored persistently in `db.json`.
* Nicely formatted console output.
* Built-in unit tests for reliability.

---

## 📦 Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/mona-raj/cli-note-app.git
cd cli-note-app
npm install
```

Link the CLI globally:

```bash
npm link
```

Now you can use the `note` command anywhere in your terminal.

---

## 🛠️ Usage

All commands are prefixed with `note`.

### 1. Create a new note

```bash
note new "clean my room" --tags "home, personal"
```

### 2. View all notes

```bash
note all
```

### 3. Find a note by keyword

```bash
note find "room"
```

### 4. Remove a note by ID

```bash
note remove <id>
```

### 5. Remove all notes

```bash
note clean
```

### 6. Open notes in the browser

```bash
note web [port]
```

* Default port: `3000`
* Uses the [`open`](https://www.npmjs.com/package/open) package to automatically launch your browser.

---

## 📂 File Structure

```
cli-note-app/
│── index.js            # Entry point
│── package.json
│── package-lock.json
│── db.json             # Stores all notes
│
├── src/
│   ├── commands.js     # CLI commands (yargs setup)
│   ├── notes.js        # Note functions (create, list, search, delete)
│   ├── db.js           # Handles JSON database interactions
│   ├── utils.js        # Utility functions (formatting, helpers)
│   └── template.js     # HTML template for web view
│
└── tests/
    └── notes.test.js   # Unit tests for notes.js
```

---

## 🧪 Running Tests

The project uses **Jest** for testing.
Run tests with:

```bash
npm test
```