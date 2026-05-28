<p align="center"><img width="240" src="lightbird/assets/logo.svg" alt="Lightbird logo"></p>

<p align="center">An elegant theme modification for Thunderbird 🐦️</p>

<p align="center"><img src="images/lightbird.webp" alt="Mockup of Lightbird"></p>

> [!WARNING]
> **This theme is currently an early work-in-progress and only light mode is supported!!** Only the Mail feature is almost finished as of now. Other parts of Thunderbird may appear broken for some time. Use at your own risk!
>
> The only functional use case for now is just reading emails and viewing calendar events.

## Version support

The theme works best on the latest stable release.

The latest ESR release may work but not guaranteed.

## Installation

Start by [downloading the latest release](https://github.com/reizumii/lightbird/archive/refs/heads/main.zip) from this repository.

1. In Thunderbird, go to **Menu > Help > Troubleshooting Information**.
2. Scroll down to the `Profile Folder` row and click `Open Folder`.
3. Inside your Thunderbird profile folder, create a new folder named `chrome`.
4. Extract the downloaded ZIP file and navigate its contents.
5. Move the extracted contents to your newly created `chrome` folder.
6. Move out the `user.js` file to your profile folder.
6. Restart Thunderbird to apply the changes.

Next, follow the [Adjustments](#adjustments) section to fully utilize Lightbird.

## Adjustments

Thunderbird 140+ now offers Mica and Acrylic transparency for Windows 11 users. To enable it, toggle the following preferences in **Advanced Preferences**.

- `widget.windows.mica` - set it to `true`.
- `widget.windows.mica.toplevel-backdrop` - set it to `1` (Mica) or `2` (Acrylic).
- **Important**: Make sure your theme is set to **System theme — auto** for it to work!

For a definitive Lightbird experience, install the following add-ons:

- [Auto Profile Picture](https://addons.thunderbird.net/thunderbird/addon/auto-profile-picture/)
- [Thunderbird Conversations](https://addons.thunderbird.net/thunderbird/addon/gmail-conversation-view/)
- [uBlock Origin](https://addons.thunderbird.net/thunderbird/addon/ublock-origin/) (optional)

## Customization

### Advanced Preferences

You can create and toggle these Boolean preferences if you feel like it.

- `lightbird.logo.hide` - hide the logo at the top-left of the window.

### Custom CSS

Lightbird heavily uses root variables stored in `lightbird/components/variables.css`. You can modify this file or as a recommendation, create a CSS file to override them and then import it using the `userChrome.css` file.

Here's a sample `custom.css` that makes Lightbird red:

```css
/* makes lightbird red */
:root {
  --selected-item-color: rgba(255, 0, 0, 0.1) !important;
  --lb-text-color: rgba(255, 0, 0) !important;
  --lb-panel-bgcolor: rgba(255, 0, 0, 0.05) !important;
}
```

And then, append this line in `userChrome.css`

```css
@import "lightbird/custom.css";
```

## Note

- **This theme is incomplete and a work-in-progress.**
- Only works with system light theme.
- Mica transparency only works on Windows.
- Untested on macOS and Linux.

## Acknowledgements

The icons used for this theme are from [Microsoft's Fluent UI System Icons](https://github.com/microsoft/fluentui-system-icons)

The bird and mail icon is derivative work based on [Microsoft's Fluent Emoji](https://github.com/microsoft/fluentui-emoji)

The font used in the Welcome page is [Instrument Serif](https://github.com/Instrument/instrument-serif)

Cloud background image by [engin akyurt](https://unsplash.com/@enginakyurt) on [Unsplash](https://unsplash.com/photos/white-clouds-under-blue-sky-during-daytime-gJILnne_HFg)
