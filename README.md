# History Manipulation Example

This repository demonstrates an example of browser **history manipulation** and how it can be exploited using JavaScript. The goal is to show how attackers can manipulate the browser history and force the user to load a different page than expected.

## Project Overview

The project includes three HTML pages:

1. **`index.html`**: The starting page where the user clicks on a link to continue.
2. **`example_of_vuln.html`**: A vulnerable page where the user is expected to click a "Go Back" button.
3. **`Hacker_page.html`**: The page that gets loaded dynamically when the user clicks "Go Back."

### Functionality

- When the user clicks "Continue" in `index.html`, they are redirected to `example_of_vuln.html`.
- The `history.pushState()` function is used in `index.html` to manipulate the browser’s history by adding `Hacker_page.html` to the history stack.
- When the user presses the "Go Back" button in `example_of_vuln.html`, they should be redirected to `Hacker_page.html`, and its content is injected into the page using JavaScript.

This demonstration shows how attackers can use **history manipulation** to alter the browser’s behavior without the user’s knowledge.

## How to Use

1. Clone the repository to your local machine.
2. Open `index.html` in a browser.
3. Click on the "Continue" link to navigate to `example_of_vuln.html`.
4. Press the "Go Back" button, and you will be redirected to `Hacker_page.html`.

## Setup Instructions

No special setup is required for this demonstration. Simply open the `index.html` file in any modern web browser to see the functionality in action.

## Key Concepts

- **History Manipulation**: Manipulating the browser’s history stack using JavaScript's `history.pushState()` function.
- **Popstate Event**: The event fired when the active history entry changes (e.g., when the user clicks the "Go Back" button).
- **Dynamic Content Injection**: Dynamically injecting content into the page without a full reload.
