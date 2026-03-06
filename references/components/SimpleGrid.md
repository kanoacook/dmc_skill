# Simplegrid

**Component**: `dmc.Simplegrid`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html

style = {
    "border": f"1px solid var(--mantine-primary-color-filled)",
    "textAlign": "center",
}

html.Div(
    # Wrapper div is added for demonstration purposes only,
    # it is not required in real projects
    dmc.SimpleGrid(
        type="container",
        cols={"base": 1, "300px": 2, "500px": 5},
        spacing={"base": 10, "300px": "xl"},
        children=[
            html.Div("1", style=style),
            html.Div("2", style=style),
            html.Div("3", style=style),
            html.Div("4", style=style),
            html.Div("5", style=style),
        ],
        p="xs",
    ),
    style={"resize": "horizontal", "overflow": "hidden", "maxWidth": "100%"},
)

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
