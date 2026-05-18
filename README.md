# Zen browser mod: Left-Aligned-Classic-Controls-in-URL-bar
This is a mod for zen browser, a Firefox's fork. Moves the tracking shield, padlock, and cookie permissions to the left side of the URL bar and tightly groups them. Removes the Zen Unified and Copy buttons.

<img width="435" height="47" alt="Screenshot 2026-05-18 at 17 32 04" src="https://github.com/user-attachments/assets/5f834aba-dd02-4cb3-870d-afb62c432bc5" />

## What the CSS code does :
- Moves the tracking protection button, padlock, and cookie permissions button to the left side of the URL bar using flex ordering.
- Removes spacing between URL bar items with `gap: 0`, which is the CSS property used to create gutters between flex items.
- Hides extra UI buttons: copy-link button, Zen unifier button, and the Firefox/Zen panel menu button via CSS selectors.

**Accessibility note**
This mod uses the CSS `order` property to change visual placement. MDN notes that `order` affects the visual order but not the underlying logical or navigation order, which can matter for accessibility and keyboard behavior.

## Settings automatically modified in advanced parameters (about:config) :
- Tells Zen Browser that it is allowed to be modified : `toolkit.legacyUserProfileCustomizations.stylesheets`, value : `true`.
- Brings back the Classic Extensions Button : `zen.theme.hide-unified-extensions-button`, value : `false`.
- Brings back the dedicated tracking shield icon : `zen.urlbar.show-protections-icon`, value : `true`.
- Removes top toolbar menu button : `zen.view.mac.show-three-dot-menu`, value : `false`.

# How to Install

## Install using Sine Theme Manager (Recommended):
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


# Tip for further development :

Activate hidden developer tool inside Zen (or Firefox) called the **Browser Toolbox**. It allows to click on any button in the browser's interface and see the exact CSS code controlling it in real-time. To enable it, go to `about:config`, search for `devtools.chrome.enabled` and `devtools.debugger.remote-enabled`, and set them both to **`true`**.
