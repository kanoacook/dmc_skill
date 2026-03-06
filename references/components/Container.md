# Container

**Component**: `dmc.Container`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html


dmc.Container(
    [
        dmc.Box("Main Content", bg="var(--mantine-color-indigo-light)", h=50),
        html.Div(
            [
                "Breakout",
                html.Div(
                    "Container inside breakout",
                    style={
                        "backgroundColor": "var(--mantine-color-indigo-filled)",
                        "color": "white",
                        "height": 50,
                    },
                    **{"data-container": ""}
                ),
            ],
            style={
                "backgroundColor": "var(--mantine-color-indigo-light)",
                "marginTop": 16,
            },
            **{"data-breakout": ""}
        ),
    ],
    size=500,
    strategy="grid",
)

---

## Props

The following props are specific to this component:

```
children, fluid, size, strategy
```

**Props count**: 4

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
