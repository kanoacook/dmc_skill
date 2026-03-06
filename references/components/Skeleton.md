# Skeleton

**Component**: `dmc.Skeleton`

**Version**: 2.6.0

---

## Overview

import time
import dash_mantine_components as dmc
from dash import  Input, Output,  html, callback, dcc

html.Div(
    [
        dcc.Loading(
            children=html.Div([
                dmc.Text("Initial data", id="dccloading-div"),
                dmc.Text("The data only takes 200ms to update, but `delay_hide` is set to 1000ms to prevent flashing.")
            ]),
            delay_hide=1000,
            custom_spinner = dmc.Skeleton(
                visible=True,
                h="100%"
            ),
        ),
        dmc.Button("Update!", id="dccloading-button"),
    ]
)

@callback(
    Output("dccloading-div", "children"),
    Input("dccloading-button", "n_clicks"),
    prevent_initial_call=True
)
def update_graph(n):
    time.sleep(.2)
    return f"Data updated {n} times"

---

## Props

The following props are specific to this component:

```
animate, children, circle, height, radius, visible, width
```

**Props count**: 7

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
