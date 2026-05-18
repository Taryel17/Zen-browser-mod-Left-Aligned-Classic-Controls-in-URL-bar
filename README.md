# Zen browser mod: Left-Aligned-Classic-Controls-in-URL-bar
This is a mod for zen browser, a Firefox's fork. Moves the tracking shield, padlock, and cookie permissions to the left side of the URL bar and tightly groups them. Removes the Zen Unified and Copy buttons.

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

## 2. Install using Sine Theme Manager (Recommended):
This mod is designed to be installed via **Sine**, the community theme manager for Zen Browser. This ensures the CSS code survives browser updates and can be easily toggled on and off.

**Step 1: Install Sine (if you haven't already)**
1. Go to the [Sine GitHub Releases page](https://github.com/CosmoCreeper/Sine/releases).
2. Download the installer for your OS (e.g., `sine-osx-arm64` for Mac M-series, or `sine-windows-amd64` for Windows).
3. Run the installer script. *(Mac users: you may need to use Terminal to remove quarantine restrictions first: `xattr -d com.apple.quarantine ./sine-osx-arm64`).*

**Step 2: Add this mod to Sine**
1. Open Zen Browser and open the newly installed **Sine** menu.
2. Look for the option to **Import from GitHub** or **Add custom theme from repository link**.
3. Type in the name of this repository: `Taryel17/Zen-browser-mod-Left-Aligned-Classic-Controls-in-URL-bar`.
4. Hit Enter. Sine will fetch the CSS and apply it automatically. 
5. Restart Zen Browser if the layout does not immediately change.
