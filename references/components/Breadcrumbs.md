# Breadcrumbs

**Component**: `dmc.Breadcrumbs`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import dcc, html

html.Div(
    [
        # default separator
        dmc.Breadcrumbs(
            children=[
                dcc.Link("Home", href="/"),
                dcc.Link("Dash Mantine Components", href="/"),
                dcc.Link("Breadcrumbs", href="/components/breadcrumbs"),
            ],
        ),
        dmc.Space(h=20),
        # separator provided
        dmc.Breadcrumbs(
            separator="→",
            children=[
                dmc.Anchor("Home", href="/", underline=False),
                dmc.Anchor("Dash Mantine Components", href="/", underline=False),
                dmc.Anchor(
                    "Breadcrumbs", href="/components/breadcrumbs", underline=False
                ),
            ],
        ),
    ]
)

---

## Props

The following props are specific to this component:

```
children, separator, separatorMargin
```

**Props count**: 3

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
