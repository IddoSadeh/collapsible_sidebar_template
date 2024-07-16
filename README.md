# Collapsible Sidebar Navigation Template

## Overview

This project provides a template for a web application with a collapsible sidebar navigation. It features a sidebar that can be populated with a directory structure, allowing for easy navigation through different pages or sections of your website.

## Features

- Collapsible sidebar with smooth animation
- Sidebar content based on a JSON file
- Clickable links in the sidebar that load content into an iframe
- Responsive design that works on various screen sizes
- Easy to customize and extend

## Project Structure
```
project-root/
│
├── index.html
├── styles.css
├── script.js
├── generate-structure.js
├── directory-structure.json
└── README.md
```

## Setup and Installation

1. Clone this repository or download the source code.
2. No server setup is required as this is a static site.

## Customization

### Adding Content

1. Add your HTML files to a `pages/` directory (you'll need to create this).
2. Update the `directory-structure.json` file to reflect your new pages.

### Styling

- Modify `styles.css` to change the appearance of the sidebar and main content area.

### Behavior

- Edit `script.js` to modify the sidebar's behavior or add new functionality.

## How It Works

- The sidebar structure is defined in `directory-structure.json`.
- The client-side JavaScript (`script.js`) fetches this JSON file and dynamically builds the sidebar navigation.
- Clicking on a file in the sidebar loads its content into the iframe in the main content area.
- The sidebar can be collapsed to a narrow strip showing only the toggle button, and expanded to show the full navigation.

## Hosting on GitHub Pages

1. Create a GitHub account if you don't have one already.
2. Create a new repository on GitHub.
3. Push your code to the GitHub repository:

```
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/yourusername/your-repo-name.git
git push -u origin master
```

4. Go to your GitHub repository settings, scroll down to the "GitHub Pages" section.
5. In the "Source" dropdown, select "master branch" and click "Save".
6. GitHub will provide you with a URL where your site is published.

## Updating the Directory Structure

To automatically update the `directory-structure.json` file based on your `pages/` directory:

1. Ensure you have Node.js installed on your system.
2. Open a terminal and navigate to your project root.
3. Run the following command:

```
node generate-structure.js
```
4. This will create or update the `directory-structure.json` file based on the current structure of your `pages/` directory.
5. Commit and push your changes to GitHub:

```
git add directory-structure.json
git commit -m "Update directory structure"
git push
```
6. Your GitHub Pages site will automatically update with the new structure.

Note: Make sure to run this script whenever you make changes to the structure of your `pages/` directory.

## Local Development

To run this project locally, you have several options:

1. **Using Python's built-in HTTP server:**
   If you have Python installed, open a command prompt in your project directory and run:
   - For Python 3: `python -m http.server 8000`
   - For Python 2: `python -m SimpleHTTPServer 8000`
   Then open your browser and go to `http://localhost:8000`

2. **Using Visual Studio Code with Live Server:**
   - Install Visual Studio Code and the "Live Server" extension
   - Open your project folder in VS Code
   - Right-click on your `index.html` file and select "Open with Live Server"

3. **Using Node.js without global installation:**
   If you have Node.js installed, open a command prompt in your project directory and run:
   ```
   npx http-server
   ```

4. **Using http-server (if execution policy allows):**
   - Install http-server globally: `npm install -g http-server`
   - Run `http-server` in your project directory

Choose the method that works best for your setup. Once the server is running, you can view and test your site locally before pushing changes to GitHub Pages.

## Browser Compatibility

This template should work in all modern browsers.

## License

This project is open-source and available under the MIT License.

## Contributing

Contributions, issues, and feature requests are welcome. Feel free to check issues page if you want to contribute.

## Support

If you have any questions or need help with customization, please open an issue in the GitHub repository.