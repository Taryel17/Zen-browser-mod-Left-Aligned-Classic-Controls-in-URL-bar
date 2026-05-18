# Left-Aligned-Classic-Controls-in-URL-bar
Moves the tracking shield, padlock, and cookie permissions to the left side of the URL bar and tightly groups them. Removes the Zen Unified and Copy buttons.

## What the CSS code does :
- Moves the tracking protection button, padlock, and cookie permissions button to the left side of the URL bar using flex ordering.
- Removes spacing between URL bar items with `gap: 0`, which is the CSS property used to create gutters between flex items.
- Hides extra UI buttons: copy-link button, Zen unifier button, and the Firefox/Zen panel menu button via CSS selectors.

**Accessibility note**
This mod uses the CSS `order` property to change visual placement. MDN notes that `order` affects the visual order but not the underlying logical or navigation order, which can matter for accessibility and keyboard behavior.

# How to Install

## 1. Required manual change in advanced parameters before applying CSS:
1. Type `about:config` into your URL bar and hit Enter. Accept the risk warning.
2. Tell Zen Browser that it is allowed to be modified : search for `toolkit.legacyUserProfileCustomizations.stylesheets` and set the value to **`true`**.
3. Bring back the Classic Extensions Button : search for: `zen.theme.hide-unified-extensions-button` and set it to **`false`**
4. Brings back the dedicated tracking shield icon : search for `zen.urlbar.show-protections-icon` and set it to **`true`**.
5. Remove top toolbar menu button : search for `zen.view.mac.show-three-dot-menu`. and set it to **`false`**.

Optional: activate hidden developer tool inside Zen (and Firefox) called the **Browser Toolbox**. It allows to click on any button in the browser's interface and see the exact CSS code controlling it in real-time. To enable it, go to `about:config`, search for `devtools.chrome.enabled` and `devtools.debugger.remote-enabled`, and set them both to **`true`**.
