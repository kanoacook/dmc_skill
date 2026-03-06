# Radarchart

**Component**: `dmc.Radarchart`

**Version**: 2.6.0

---

## Overview

from random import randint
import dash_mantine_components as dmc
from dash import callback, Input, Output

dmc.Box(
    [
        dmc.Button("Update Chart", id="btn-radarchart-animation"),
        dmc.RadarChart(
            id="radarchart-animation",
            h=300,
            data=[{}],
            dataKey="product",
            withPolarRadiusAxis=True,
            radarProps={
                "isAnimationActive": True,
            },
            series=[{"name": "sales", "color": "blue.4", "opacity": 0.2}],
        ),
    ]
)


@callback(
    Output("radarchart-animation", "data"),
    Input("btn-radarchart-animation", "n_clicks"),
)
def update(n):
    return [
        {"product": "Apples", "sales": randint(20, 100)},
        {"product": "Oranges", "sales": randint(20, 100)},
        {"product": "Tomatoes", "sales": randint(20, 100)},
        {"product": "Grapes", "sales": randint(20, 100)},
        {"product": "Bananas", "sales": randint(20, 100)},
        {"product": "Lemons", "sales": randint(20, 100)},
    ]

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
