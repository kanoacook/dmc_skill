# Compositechart

**Component**: `dmc.Compositechart`

**Version**: 2.6.0

---

## Overview

from dash import callback, Input, Output
import dash_mantine_components as dmc
from .data import data

dmc.Group(
    [
        dmc.CompositeChart(
            id="figure-compositechart-hover",
            h=300,
            data=data,
            dataKey="date",
            withLegend=True,
            maxBarWidth=30,
            series=[
                {"name": "Tomatoes", "color": "rgba(18, 120, 255, 0.2)", "type": "bar"},
                {"name": "Apples", "color": "red.8", "type": "line"},
                {"name": "Oranges", "color": "yellow.8", "type": "area"},
            ]
        ),
        dmc.Text(id="hoverdata-compositechart1"),
        dmc.Text(id="hoverdata-compositechart2"),
    ]
)

@callback(
    Output("hoverdata-compositechart1", "children"),
    Output("hoverdata-compositechart2", "children"),
    Input("figure-compositechart-hover", "hoverData"),
    Input("figure-compositechart-hover", "hoverSeriesName"),
)
def update(data, name):
    return f"hoverData:  {data}", f"hoverSeriesName: {name}"

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
