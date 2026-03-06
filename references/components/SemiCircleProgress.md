# Semicircleprogress

**Component**: `dmc.Semicircleprogress`

**Version**: 2.6.0

---

## Overview

import random
import dash_mantine_components as dmc
from dash import Input, Output, callback

dmc.Box([
    dmc.SemiCircleProgress(value=30, transitionDuration=250, label="30%", id="semi-circle-progress"),
    dmc.Button("Set random value", mt="md", ml=22, id="semi-circle-progress-btn"),

])

@callback(
    Output("semi-circle-progress", "value"),
    Output("semi-circle-progress", "label"),
    Input("semi-circle-progress-btn", "n_clicks")
)
def update(n):
    number = random.randint(1, 100)
    return number, f"{number}%"

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
