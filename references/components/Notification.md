# Notification

**Component**: `dmc.Notification`

**Version**: 2.6.0

---

## Overview

from dash import Input, Output, callback, no_update
import dash_mantine_components as dmc

dmc.Group(
    justify="center",
    children=[
        dmc.Button("Closes in 4 seconds", id="default-close-btn", n_clicks=0),
        dmc.Button("Closes in 500ms", id="short-close-btn", n_clicks=0),
        dmc.Button("Never closes automatically", id="no-autoclose-btn", n_clicks=0),
      #  dmc.NotificationsContainer(id="notification-container"),
    ]
)


@callback(
    Output("notification-container", "sendNotifications", allow_duplicate=True),
    Input("default-close-btn", "n_clicks"),
    prevent_initial_call=True
)
def short_notification(n):
    if n > 0:
        return [{
            "action": "show",
            "message": "I will close in 4 seconds (the default auto close)",

        }]
    return no_update

@callback(
    Output("notification-container", "sendNotifications", allow_duplicate=True),
    Input("short-close-btn", "n_clicks"),
    prevent_initial_call=True
)
def short_notification(n):
    if n > 0:
        return [{
            "action": "show",
            "message": "I will close in 500ms",
            "autoClose": 500,
        }]
    return no_update


@callback(
    Output("notification-container", "sendNotifications", allow_duplicate=True),
    Input("no-autoclose-btn", "n_clicks"),
    prevent_initial_call=True
)
def sticky_notification(n):
    if n > 0:
        return [{
            "action": "show",
            "title": "I will never close",
            "message": "unless you click X",
            "color": "blue",
            "autoClose": False,
            "style": {"marginBottom": 20}
        }]
    return no_update

---

## Props

The following props are specific to this component:

```
action, autoClose, closeButtonProps, color, icon, loading, message, position, radius, title, withBorder, withCloseButton
```

**Props count**: 12

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
