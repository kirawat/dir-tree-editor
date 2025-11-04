# DirTreeEditor

**DirTreeEditor** is a single-file, zero-dependency HTML application for creating, editing, and sharing directory tree diagrams.

It provdes a simple, text-based editor on one side and a live formatted tree preview on the other, all in a portable, offline-first app.

## How to Use

The application is split into two panes for a simple workflow:

1. **Editor (Left Pane):** Write your directory structure using plain indented text.

2. **Preview (Right Pane):** See the beautifully formatted tree render instantly as you type.

### The Editing Convention

- **Indentation:** Use simple indentation (with spaces) to define your hierarchy. The app will auto-detect your indent size (1-4 spaces).

- **Defining Folders (Important):** To explicitly mark something as a folder (especially an empty one), add a trailing slash (`/`).

- **Defining Files:** Any item *without* a trailing slash and *without* children is treated as a file.

**Example Input:**

```
my-project/
    src/
        index.html
        style.css
    dist/
    LICENSE
    README.md
```

**Example Output:**

```
📁 my-project/
├── 📁 src/
│   ├── 📄 index.html
│   └── 📄 style.css
├── 📁 dist/
├── 📄 LICENSE
└── 📄 README.md
```

## Features

### Smart Editor

- **Smart Tab:** Pressing `Tab` inserts the auto-detected indentation (e.g., 4 spaces) instead of changing focus.

- **Smart Enter:** Pressing `Enter` creates a new line that automatically matches the indentation of the line above.

- **Smart Backspace:** Pressing `Backspace` at the start of an indented line deletes one full "indent chunk" at a time.

- **Indent Detection:** Automatically detects if your structure uses 1, 2, 3, or 4 spaces for indentation and adapts all "Smart" features accordingly.

- **Smart Paste:** Automatically cleans up pre-formatted tree text that you paste, stripping `├──`, `└──`, icons, and extra slashes.

### Live Preview & Customization

- **Instant Render:** The preview pane updates on every keystroke.

- **Trailing Slash:** Toggle to automatically add trailing slashes (`/`) to folders in the preview.

- **Icons:** Toggle to show 📁 and 📄 icons for folders and files.

- **Preserves Blank Lines:** Respects blank lines in your editor for spacing out projects.

### Tools & Sharing

- **Sort:** Instantly sort your entire tree alphabetically, level by level, with a single click.

- **Copy:** A dedicated button to copy the clean, formatted preview text to your clipboard.

- **Saveable & Shareable URLs:** The app saves your *entire* text content (Base64-encoded) and your options directly into the URL.

- **Share Button:** A simple button to copy the shareable URL, allowing you to send your exact tree and settings to others.

- **URL-based Settings:** You can manually set options via URL parameters (e.g., `?trailing=1&icons=0).

### Portability

- **Single File:** The entire application is contained in a single `.html` file.

- **Works Offline:** No external dependencies, libraries, or internet connection required.

- **Cross-Browser:** Runs in any modern web browser.

## Contributing

Contributions are welcome. Since this is a single-file application, you can fork the repository, make your changes directly to the `dir-tree-editor.html` file, and open a pull request.

If you find a bug or have a feature request, please open an issue. Thank you!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
