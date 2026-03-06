# Timegrid

**Component**: `dmc.Timegrid`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import callback, Input, Output

dmc.Stack([
    dmc.TimeGrid(
        timeRangeData={"startTime": "10:00", "endTime": "21:00", "interval": "01:00"},
        withSeconds=False,
        simpleGridProps={
            "type": "container",
            "cols": {"base": 1, "180px": 2, "320px": 3},
            "spacing": "xs",
        },
        value="10:00:00",
        id="time-grid"
    ),
    dmc.Text(id="time-grid-out")
])

@callback(
    Output("time-grid-out", "children"),
    Input("time-grid", "value")
)
def update(value):
    return f"You selected: {value}"

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
