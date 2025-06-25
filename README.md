# Favorite Icon Toggler

This project is a simple, interactive web application for toggling favorite icons. Users can click on heart icons next to items to mark them as favorites. Clicking the icon toggles between an empty heart (`♡`) and a filled heart (`❤`).

---

## Features

* **Interactive Buttons**: Users can toggle favorite status by clicking the heart icons next to each item.
* **Dynamic Updates**: The heart icon changes from empty (`♡`) to filled (`❤`) when toggled.
* **Visual Feedback**: The filled heart changes color to red, providing clear feedback.

---

## File Structure

```
├── index.html       # Main HTML file containing the structure
├── styles.css       # CSS file for styling
├── script.js        # JavaScript file for interactivity
```

---

## Code Overview

### HTML (`index.html`)

* Contains a list of art supplies with a favorite button (`&#9825;`) next to each item.
* The button has a `favorite-icon` class to enable event handling.

```html
<ul class="item-list">
  <li>120 gm paper<button class="favorite-icon">&#9825;</button></li>
  <li>Watercolor set<button class="favorite-icon">&#9825;</button></li>
  <li>Lead pencil 6B<button class="favorite-icon">&#9825;</button></li>
</ul>
```

---

### CSS (`styles.css`)

* **`button`**: Styled with a large font size and no background or border for a clean look.
* **`.filled`**: Adds a red color and bold style to indicate the "favorite" state.

```css
.filled {
  color: red;
  font-size: 1.5rem;
  font-weight: bold;
}
```

---

### JavaScript (`script.js`)

* Selects all elements with the `favorite-icon` class.
* Adds a `click` event listener to each button.
* Toggles the `filled` class and updates the button content dynamically.

```javascript
const heartButtons = document.querySelectorAll(".favorite-icon");

heartButtons.forEach((button) => {
  button.addEventListener("click", () => {
    if (button.classList.contains("filled")) {
      button.classList.remove("filled");
      button.innerHTML = "&#9825;"; // Empty heart
    } else {
      button.classList.add("filled");
      button.innerHTML = "&#10084;"; // Filled heart
    }
  });
});
```

---

## Usage

1. Open the `index.html` file in a web browser.
2. Click the heart icon next to any item in the list.

   * Empty heart (`♡`) toggles to filled heart (`❤`) and vice versa.
   * Filled hearts are styled with the `.filled` class.

---

## Technologies Used

* **HTML5**: Provides the structure for the item list and buttons.
* **CSS3**: Adds styling for layout, typography, and button states.
* **JavaScript**: Implements interactivity and dynamic updates.

---

## Potential Improvements

* Add functionality to save the favorite state (e.g., using local storage).
* Provide animations for a smoother toggle effect.
* Allow users to filter the list based on favorites.

---

## Author

Developed by \Oluwatobiloba. This simple app demonstrates dynamic styling and event-driven interactions.
