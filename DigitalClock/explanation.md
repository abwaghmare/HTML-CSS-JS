# Digital Clock Project

This document explains the structure, styling, and functionality of the Digital Clock project.

## HTML: Structure of the Web Page

### Document Declaration (`<!DOCTYPE html>`)
- Declares the document as HTML5.

### Head Section (`<head>`)
- Contains metadata and other information about the page.
- Includes:
    - `<title>`: Sets the page's title to "Digital Clock".
    - `<style>`: Contains CSS for styling.

### Body Section (`<body>`)
- Displays the content visible to users.
- Includes:
    - A `<div>` with `id="digitalclock"`: Dynamically displays the clock's time.
    - A `<h1>` heading: Displays the title "Digital Clock".

---

## CSS: Styling the Page

### Body Styling
- Centers content using Flexbox (`display: flex`).
- Sets a gradient background transitioning between shades of blue.
- Text color is white (`color: #ffffff`).

### Heading Styling (`<h1>`)
- Centered with a shadow (`text-shadow`).
- Larger font size for emphasis.

### Clock Styling (`#digitalclock`)
- Large, bold font (`font-size: 3rem; font-weight: bold`).
- Rounded corners (`border-radius: 10px`) and a semi-transparent border.
- Subtle shadow (`box-shadow`) for a 3D effect.
- Semi-transparent background (`background: rgba(255, 255, 255, 0.1)`).

---

## JavaScript: Adding Functionality

### `showTime` Function
- Fetches the current time and updates the clock every second.

#### Key Steps:
1. **Get Current Time**:
     - Uses `new Date()` to fetch the current date and time.
     - Extracts hours, minutes, and seconds using `getHours()`, `getMinutes()`, and `getSeconds()`.

2. **AM/PM Formatting**:
     - Converts 24-hour format to 12-hour format.
     - Sets "AM" or "PM" based on the time.

3. **Time Formatting**:
     - Adds leading zeros for single-digit hours, minutes, or seconds (e.g., `12:05:09`).

4. **Update Clock Display**:
     - Inserts the formatted time into the `<div>` with `id="digitalclock"` using:
         ```javascript
         document.getElementById("digitalclock").textContent = time;
         ```

5. **Refresh Clock**:
     - Uses `setTimeout(showTime, 1000)` to update the clock every second.

### Initializing the Clock
- Calls `showTime()` once to start the clock, which then updates itself every second.

---

This project demonstrates the integration of HTML, CSS, and JavaScript to create a functional and visually appealing digital clock.