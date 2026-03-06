# Piechart

**Component**: `dmc.Piechart`

**Version**: 2.6.0

---

## Overview

from random import randint
import dash_mantine_components as dmc
from dash import callback, Input, Output


def get_data(values):
    return [
        {"name": "A", "value": values[0], "color": "indigo.6"},
        {"name": "B", "value": values[1], "color": "yellow.6"},
        {"name": "C", "value": values[2], "color": "teal.6"},
        {"name": "C", "value": values[3], "color": "gray.6"},
    ]


dmc.Box(
    [
        dmc.Button("Update Chart", id="btn-piechart-animation", n_clicks=0, mb="md"),
        dmc.PieChart(
            id="piechart-animation",
            data=get_data([100, 0, 0, 0]),
            pieProps={"isAnimationActive": True},
        ),
    ]
)


@callback(
    Output("piechart-animation", "data"), Input("btn-piechart-animation", "n_clicks")
)
def update(n):
    if n % 2 == 0:
        return get_data([400, 300, 600, 100])
    return get_data([100, 0, 0, 0])

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
