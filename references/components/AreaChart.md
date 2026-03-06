# Areachart

**Component**: `dmc.Areachart`

**Version**: 2.6.0

---

## Overview

from random import randint
import dash_mantine_components as dmc
from dash import callback, Input, Output

dmc.Box(
    [
        dmc.Button("Update Chart", id="btn-areachart-animation"),
        dmc.AreaChart(
            id="areachart-animation",
            h=300,
            dataKey="date",
            data=[{}],
            tooltipAnimationDuration=500,
            areaProps={
                "isAnimationActive": True,
                "animationDuration": 500,
                "animationEasing": "ease-in-out",
                "animationBegin": 500,
            },
            series=[
                {"name": "Apples", "color": "indigo.6"},
                {"name": "Oranges", "color": "blue.6"},
                {"name": "Tomatoes", "color": "teal.6"},
            ],
        ),
    ]
)


@callback(
    Output("areachart-animation", "data"), Input("btn-areachart-animation", "n_clicks")
)
def update(n):
    return [
        {
            "date": "Mar 22",
            "Apples": 2890,
            "Oranges": 2338,
            "Tomatoes": randint(1000, 4000),
        },
        {
            "date": "Mar 23",
            "Apples": 2756,
            "Oranges": 2103,
            "Tomatoes": randint(1000, 4000),
        },
        {
            "date": "Mar 24",
            "Apples": 3322,
            "Oranges": 986,
            "Tomatoes": randint(1000, 4000),
        },
        {
            "date": "Mar 25",
            "Apples": 3470,
            "Oranges": 2108,
            "Tomatoes": randint(1000, 4000),
        },
        {
            "date": "Mar 26",
            "Apples": 3129,
            "Oranges": 1726,
            "Tomatoes": randint(1000, 4000),
        },
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
