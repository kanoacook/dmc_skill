# Richtexteditor

**Component**: `dmc.Richtexteditor`

**Version**: 2.6.0

---

## Overview

default_labels = {
    # Controls labels
    "linkControlLabel": "Link",
    "colorPickerControlLabel": "Text color",
    "highlightControlLabel": "Highlight text",
    "colorControlLabel": "Set text color {color}",  # Use f-string format to include color in label
    "boldControlLabel": "Bold",
    "italicControlLabel": "Italic",
    "underlineControlLabel": "Underline",
    "strikeControlLabel": "Strikethrough",
    "clearFormattingControlLabel": "Clear formatting",
    "unlinkControlLabel": "Remove link",
    "bulletListControlLabel": "Bullet list",
    "orderedListControlLabel": "Ordered list",
    "h1ControlLabel": "Heading 1",
    "h2ControlLabel": "Heading 2",
    "h3ControlLabel": "Heading 3",
    "h4ControlLabel": "Heading 4",
    "h5ControlLabel": "Heading 5",
    "h6ControlLabel": "Heading 6",
    "blockquoteControlLabel": "Blockquote",
    "alignLeftControlLabel": "Align text: left",
    "alignCenterControlLabel": "Align text: center",
    "alignRightControlLabel": "Align text: right",
    "alignJustifyControlLabel": "Align text: justify",
    "codeControlLabel": "Code",
    "codeBlockControlLabel": "Code block",
    "subscriptControlLabel": "Subscript",
    "superscriptControlLabel": "Superscript",
    "unsetColorControlLabel": "Unset color",
    "hrControlLabel": "Horizontal line",
    "undoControlLabel": "Undo",
    "redoControlLabel": "Redo",

    # Task list
    "tasksControlLabel": "Task list",
    "tasksSinkLabel": "Decrease task level",
    "tasksLiftLabel": "Increase task level",

    # Link editor
    "linkEditorInputLabel": "Enter URL",
    "linkEditorInputPlaceholder": "https://example.com/",
    "linkEditorExternalLink": "Open link in a new tab",
    "linkEditorInternalLink": "Open link in the same tab",
    "linkEditorSave": "Save",

    # Color picker control
    "colorPickerCancel": "Cancel",
    "colorPickerClear": "Clear color",
    "colorPickerColorPicker": "Color picker",
    "colorPickerPalette": "Color palette",
    "colorPickerSave": "Save",
    "colorPickerColorLabel": "Set Text color {color}",  # Use f-string format to include color in color swatch label
}

---

## Props

The following props are specific to this component:

```
(See all-components.md for details)
```

**Props count**: 0

---

## Shared Props (All Components)

These props work on **every DMC component** and don't need to be listed per-component:

**Spacing**: `m`, `my`, `mx`, `mt`, `mb`, `ml`, `mr`, `ms`, `me`, `p`, `py`, `px`, `pt`, `pb`, `pl`, `pr`, `ps`, `pe`
**Sizing**: `w`, `h`, `miw`, `maw`, `mih`, `mah`
**Color**: `c`, `bg`
**Position**: `pos`, `top`, `left`, `bottom`, `right`, `inset`
**Display**: `display`, `flex`, `opacity`
**Typography**: `ff`, `fz`, `fw`, `lts`, `ta`, `lh`, `fs`, `tt`, `td`
**Borders**: `bd`, `bdrs`, `bgsz`, `bgp`, `bgr`, `bga`
**Visibility**: `hiddenFrom`, `visibleFrom`, `lightHidden`, `darkHidden`
**Theming**: `classNames`, `styles`, `unstyled`, `variant`
**System**: `id`, `className`, `style`, `tabIndex`, `mod`, `attributes`

---

## See Also

- **Full reference**: `references/all-components.md`
- **Component index**: `references/components/INDEX.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
