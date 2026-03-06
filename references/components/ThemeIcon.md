# Themeicon

**Component**: `dmc.Themeicon`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify

dmc.Group(
    children=[
        dmc.ThemeIcon(
            DashIconify(icon="tabler:photo", width=20),
            variant="gradient",
            gradient={"from": "indigo", "to": "cyan"},
            size="lg",
        ),
        dmc.ThemeIcon(
            DashIconify(icon="tabler:photo", width=20),
            variant="gradient",
            gradient={"from": "teal", "to": "lime", "deg": 105},
            size="lg",
        ),
        dmc.ThemeIcon(
            DashIconify(icon="tabler:photo", width=20),
            variant="gradient",
            gradient={"from": "teal", "to": "blue", "deg": 60},
            size="lg",
        ),
        dmc.ThemeIcon(
            DashIconify(icon="tabler:photo", width=20),
            variant="gradient",
            gradient={"from": "orange", "to": "red"},
            size="lg",
        ),
        dmc.ThemeIcon(
            DashIconify(icon="tabler:photo", width=20),
            variant="gradient",
            gradient={"from": "grape", "to": "pink", "deg": 35},
            size="lg",
        ),
    ]
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
