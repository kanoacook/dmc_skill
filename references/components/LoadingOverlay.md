# Loadingoverlay

**Component**: `dmc.Loadingoverlay`

**Version**: 2.6.0

---

## Overview

import time

import dash_mantine_components as dmc
from dash import Output, Input, no_update, callback, clientside_callback
from dash_iconify import DashIconify

dmc.Box(
    children=[
        dmc.Stack(
            pos="relative",
            p=5,
            w=300,
            children=[
                dmc.LoadingOverlay(
                    visible=False,
                    id="loading-overlay",
                    overlayProps={"radius": "sm", "blur": 2},
                    zIndex=10,
                ),
                dmc.TextInput(
                    label="Username",
                    placeholder="Your username",
                    leftSection=DashIconify(icon="radix-icons:person"),
                    id="dummy-text-box",
                ),
                dmc.TextInput(
                    label="Password",
                    placeholder="Your password",
                    leftSection=DashIconify(icon="radix-icons:lock-closed"),
                ),
                dmc.Checkbox(
                    label="Remember me",
                    checked=True,
                ),
                dmc.Button(
                    "Login", id="load-button", variant="outline", fullWidth=True
                ),
            ],
        ),
    ]
)

clientside_callback(
    """
    function updateLoadingState(n_clicks) {
        return true
    }
    """,
    Output("loading-overlay", "visible", allow_duplicate=True),
    Input("load-button", "n_clicks"),
    prevent_initial_call=True,
)


@callback(
    Output("dummy-text-box", "children"),
    Output("loading-overlay", "visible"),
    Input("load-button", "n_clicks"),
    prevent_initial_call=True,
)
def update(n_clicks):
    time.sleep(3)
    return no_update, False

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
