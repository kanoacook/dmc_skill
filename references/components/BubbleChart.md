# Bubblechart

**Component**: `dmc.Bubblechart`

**Version**: 2.6.0

---

## Overview

from dash import callback, Input, Output
import dash_mantine_components as dmc
from .data import data

dmc.Group(
    [
        dmc.BubbleChart(
            id="figure-bubblechart-hover",
            gridColor="gray.5",
            textColor="gray.9",
            h=60,
            data=data,
            range=[16, 225],
            label="Sales/hour",
            color="lime.6",
            dataKey={"x": "hour", "y": "index", "z": "value"}
        ),
        dmc.Text(id="hoverdata-bubblechart"),

    ]
)

@callback(
    Output("hoverdata-bubblechart", "children"),
    Input("figure-bubblechart-hover", "hoverData"),
)
def update(data):
    return f"hoverData:  {data}"

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
