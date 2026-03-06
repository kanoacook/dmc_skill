# Overlay

**Component**: `dmc.Overlay`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import Dash, Input, Output, callback, html


dmc.Stack([
        dmc.AspectRatio(
            ratio=16/9,
            maw=400,
            mx="auto",
            pos="relative",
            children=[
                html.Img(
                    src="https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/images/bg-7.png",
                    alt="Demo",
                ),
                dmc.Overlay(
                    id="overlay-gradient",
                    gradient="linear-gradient(145deg, rgba(0, 0, 0, 0.95) 0%, rgba(0, 0, 0, 0) 100%)",
                    opacity=0.85,
                    style={"display": "block"}  # Initially visible
                )
            ]
        ),
        dmc.Button(
            "Toggle overlay",
            id="overlay-toggle-button-gradient",
            mx="auto",
            mt="lg",
            n_clicks=0
        )
    ])


@callback(
    Output("overlay-gradient", "style"),
    Input("overlay-toggle-button-gradient", "n_clicks")
)
def toggle_overlay(n_clicks):
    if n_clicks %2 == 0:
        return {"display": "block"}
    return {"display": "none"}

---

## Props

The following props are specific to this component:

```
backgroundOpacity, blur, center, children, color, fixed, gradient, radius, zIndex
```

**Props count**: 9

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
