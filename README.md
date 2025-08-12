Responsive Bookstore Website
A simple static website for a bookstore, designed to be responsive using CSS media queries. The site features a navigation bar, a two-column layout (main content and sidebar), and an image, optimized for both desktop and mobile viewports.
Objective
Convert a desktop-only webpage into a mobile-friendly layout using CSS media queries, ensuring proper stacking of elements, reduced font sizes, a collapsible navigation menu, and scaled images for mobile devices (max-width: 768px).
Prerequisites

Browser: Google Chrome (for testing with DevTools).
VS Code: For editing HTML and CSS files (optional, any text editor works).
Node.js (optional): For running a local server to test the site dynamically.
Chrome DevTools: To test the mobile layout.

Setup Instructions

Create the Project Directory:

Create a folder (e.g., bookstore-website) inside C:\Users\Admin\OneDrive\Desktop\labs or your preferred location.
Navigate to the directory:cd C:\Users\Admin\OneDrive\Desktop\labs\bookstore-website




Add the Files:

Save the provided index.html file in the project directory.
Save the provided styles.css file in the same directory.
Ensure the <link rel="stylesheet" href="styles.css"> in index.html points to the correct CSS file.


View the Website:

Open index.html directly in Google Chrome by double-clicking the file, or:
Use a local server for a more realistic test:npx http-server


Access the site at http://localhost:8080 (port may vary, check the terminal output).





Project Structure
bookstore-website/
├── index.html       # HTML file for the bookstore website
├── styles.css       # CSS with desktop and mobile styles (media queries)

Features

Desktop Layout:
Horizontal navigation bar with links (Home, Books, About, Contact).
Two-column layout: main content (70% width) and sidebar (30% width).
Fixed-width container (1200px) and image (600px max-width).


Mobile Layout (max-width: 768px):
Columns stack vertically (main content above sidebar).
Navigation menu collapses to a vertical stack.
Font sizes reduced for better readability.
Images scale to fit the viewport (max-width: 100%).
Overflow and scrolling issues fixed with overflow-x: hidden and box-sizing: border-box.



Testing with Chrome DevTools

Open index.html in Google Chrome.
Launch DevTools:
Press F12 or right-click and select "Inspect".


Enable the Device Toolbar:
Click the phone/tablet icon in the top-left corner of DevTools.
Select a mobile device (e.g., "iPhone SE") or set a custom viewport width (e.g., 768px or less).


Verify the mobile layout:
Navigation menu items stack vertically.
Main content and sidebar are stacked vertically.
Fonts are smaller (e.g., h1 at 28px, p at 14px).
Image fits within the screen width without overflow.
No horizontal scrolling occurs.



CSS Media Query Details
The styles.css file includes media queries targeting max-width: 768px to adjust:

Container: Switches from fixed 1200px to 100% width with flex-direction: column.
Navigation: Changes from horizontal to vertical with flex-direction: column.
Fonts: Reduces sizes for h1, h2, and p.
Images: Sets max-width: 100% to ensure scaling.
Overflow: Uses overflow-x: hidden on body and overflow: auto on content sections to prevent scrolling issues.

Troubleshooting

Image Not Scaling: Ensure img { max-width: 100%; height: auto; } is in the media query.
Horizontal Scrolling: Check for fixed-width elements outside the media query; adjust to percentage-based widths.
Navigation Not Collapsing: Verify .nav-menu { flex-direction: column; } in the media query.
Server Issues: If using npx http-server, ensure Node.js is installed (node -v should show a version, e.g., 22.15.0). Install Node.js from nodejs.org if needed.

Notes

The meta viewport tag in index.html ensures proper scaling on mobile devices.
Data is static; for dynamic content, integrate with the Books REST API from Task 3.
For production, host the site on a server (e.g., using Express) and test on actual mobile devices.
