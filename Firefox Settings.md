## Enable Custom Stylesheets
Goto: `about:config`

Enable:
```
toolkit.legacyUserProfileCustomizations.stylesheets
```

Goto: `about:support`

seach for `profile` word and open profile folder.

## Clean right click context menu
In profile folder create `chrome` folder and inside it create `userChrome.css`

```css
/* Hide "Open in Split View" */
#context-openlinkinsplitview {
    display: none !important;
}

/* Hide "Open in New Container Tab" */
#context-openlinkinusercontext-menu {
	display: none !important;
}

/* Hide "Preview Link" */
#context-previewlink {
    display: none !important;
}

/* Hide "Bookmark Link" */
#context-bookmarklink {
    display: none !important;
}

/* Hide "Send Link to Device" and its separator line */
#context-sendlinktodevice, 
#context-sep-sendlinktodevice,

/* Hide "Send Page to Device" and its separator line */
#context-sendpagetodevice, 
#context-sep-sendpagetodevice,

/* Hide "Send Tab to Device" (from tab right-clicks) */
#context_sendTabToDevice, 
#context_sendTabToDevice_separator {
    display: none !important;
}

/* Hide "Search Google for" */
#context-searchselect {
    display: none !important;
}

/* Hide "Translate Text to" */
#context-translate-selection {
    display: none !important;
}

/* Hide "Inspect Accesibility Options" */
#context-inspect-a11y {
    display: none !important;
}

/* Hide "Email image" */
#context-sendimage {
    display: none !important;
}

/* Hide "Search Image with Google Lens" */
#context-visual-search {
    display: none !important;
}

/* Hide "Set image as desktop background" */
#context-setDesktopBackground { 
    display: none !important; 
}

/* Hide the line separator directly below it */
#context-sep-setbackground {
    display: none !important;
}

/* Hide separator under Copy Clean Link */
#frame-sep {
  display: none !important;
}
```

## Change system-ui font to SegoeUI, [source](https://connect.mozilla.org/t5/ideas/change-the-handling-of-quot-font-family-system-ui-quot/idi-p/11900)
Goto: `about:config`

Disable:
```
layout.css.system-ui.enabled
```

Inside chrome folder create `userContent.css`

```css
@font-face {
    font-family: system-ui;
    src: local("Segoe UI");
    font-weight: 100 1000;
    font-style: normal;
}
@font-face {
    font-family: system-ui;
    src: local("Segoe UI");
    font-weight: 100 1000;
    font-style: italic;
}
```
