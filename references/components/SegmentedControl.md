# Segmentedcontrol

**Component**: `dmc.Segmentedcontrol`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import Output, Input, html, callback
from dash_iconify import DashIconify

data = [
    ["Preview", "tabler:eye"],
    ["Code", "tabler:code"],
    ["Export", "tabler:external-link"],
]

html.Div(
    [
        dmc.SegmentedControl(
            id="segmented-with-react-nodes",
            value="Preview",
            data=[
                {
                    "value": v,
                    "label": dmc.Center(
                        [DashIconify(icon=icon, width=16), html.Span(v)],
                        style={"gap": 10},
                    ),
                }
                for v, icon in data
            ],
            mb=10,
        ),
        dmc.Text(id="segmented--value-data"),
    ]
)


@callback(
    Output("segmented--value-data", "children"),
    Input("segmented-with-react-nodes", "value"),
)
def update_value(value):
    return value

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
