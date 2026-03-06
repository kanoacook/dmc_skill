# Modal

**Component**: `dmc.Modal`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html, Output, Input, callback, ctx, no_update


dmc.Center([
    dmc.ModalStack(
        id="modal-stack",
        children=[
            dmc.ManagedModal(
                id="delete-page",
                title="Delete this page?",
                children=[
                    dmc.Text("Are you sure you want to delete this page? This action cannot be undone."),
                    dmc.Group(
                        mt="lg",
                        justify="flex-end",
                        children=[
                            dmc.Button("Cancel", id="cancel-1", variant="default"),
                            dmc.Button("Delete", id="delete", color="red"),
                        ],
                    ),
                ],
            ),
            dmc.ManagedModal(
                id="confirm-action",
                title="Confirm action",
                children=[
                    dmc.Text("Are you sure you want to perform this action? This action cannot be undone. If you are sure, press confirm button below."),
                    dmc.Group(
                        mt="lg",
                        justify="flex-end",
                        children=[
                            dmc.Button("Cancel", id="cancel-2", variant="default"),
                            dmc.Button("Confirm", id="confirm", color="red"),
                        ],
                    ),
                ],
            ),
            dmc.ManagedModal(
                id="really-confirm-action",
                title="Really confirm action",
                children=[
                    dmc.Text("Jokes aside. You have confirmed this action. This is your last chance to cancel it. After you press confirm button below, action will be performed and cannot be undone. For real this time. Are you sure you want to proceed?"),
                    dmc.Group(
                        mt="lg",
                        justify="flex-end",
                        children=[
                            dmc.Button("Cancel", id="cancel-3", variant="default"),
                            dmc.Button("Confirm", id="final-confirm", color="red"),
                        ],
                    ),
                ],
            ),
        ]
    ),
    dmc.Button("Open modal", id="open")
])


@callback(
    Output("modal-stack", "open"),
    Output("modal-stack", "closeAll"),
    Input("open", "n_clicks"),
    Input("cancel-1", "n_clicks"),
    Input("cancel-2", "n_clicks"),
    Input("cancel-3", "n_clicks"),
    Input("delete", "n_clicks"),
    Input("confirm", "n_clicks"),
    Input("final-confirm", "n_clicks"),
    prevent_initial_call=True,
)
def control_modals(*_):
    trigger = ctx.triggered_id
    if trigger == "open":
        return "delete-page", False
    if trigger in ("cancel-1", "cancel-2", "cancel-3", "final-confirm"):
        return None, True
    if trigger == "delete":
        return "confirm-action", False
    if trigger == "confirm":
        return "really-confirm-action", False
    return no_update, no_update

---

## Props

The following props are specific to this component:

```
centered, children, closeButtonProps, closeOnClickOutside, closeOnEscape, fullScreen, keepMounted, lockScroll, opened, overlayProps, padding, portalProps, radius, removeScrollProps, returnFocus, shadow, size, title, transitionProps, trapFocus, withCloseButton, withOverlay, withinPortal, xOffset, yOffset, zIndex
```

**Props count**: 26

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
