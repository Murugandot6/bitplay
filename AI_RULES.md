# AI Rules for BitPlay Development

This document outlines the core technologies and specific library usage guidelines for developing the BitPlay web application.

## Tech Stack

*   **Frontend Language**: Vanilla JavaScript (ES6+) for all client-side logic and DOM manipulation.
*   **Markup**: HTML5.
*   **Styling**: Tailwind CSS for all visual styling and responsive design.
*   **Video Playback**: Video.js for the embedded video player.
*   **Video Player Enhancements**: Video.js Hotkeys plugin for keyboard controls.
*   **Notifications**: Butterup for displaying toast messages and alerts.
*   **Icons**: Lucide Icons for all SVG iconography.
*   **Backend Language**: Go (as indicated by the project structure and README).
*   **API Communication**: RESTful API calls using the native `fetch` API.
*   **Build Tools**: Tailwind CSS CLI for processing CSS.

## Library Usage Rules

To maintain consistency and simplicity, please adhere to the following rules when introducing or modifying code:

*   **Frontend Frameworks**: Do NOT introduce any frontend frameworks (e.g., React, Vue, Angular). All frontend logic must be implemented using **Vanilla JavaScript**.
*   **Styling**:
    *   Always use **Tailwind CSS** utility classes for styling.
    *   Avoid writing custom CSS unless absolutely necessary for complex animations or specific overrides that cannot be achieved with Tailwind. If custom CSS is needed, it should be minimal and well-justified.
*   **Icons**: Use **Lucide Icons** for all graphical icons. Do not introduce other icon libraries.
*   **Video Player**: The video player functionality is handled by **Video.js**. Use its API and existing plugins (like `videojs.hotkeys.min.js`) for any player-related features. Do not introduce other video player libraries.
*   **Notifications**: For all user notifications (success, error, info, warning messages), use the **Butterup** library.
*   **DOM Manipulation**: Stick to native **Vanilla JavaScript** methods for interacting with the DOM (e.g., `document.querySelector`, `addEventListener`, `createElement`, `classList` manipulation). Do not introduce libraries like jQuery.
*   **Routing**: The application currently handles routing via URL query parameters. Do not introduce a dedicated client-side routing library unless a significant architectural shift explicitly requires it.
*   **Dependencies**: Only add new dependencies if absolutely necessary and after careful consideration that the functionality cannot be achieved with existing libraries or vanilla JavaScript. Prioritize small, focused libraries over large, opinionated ones.