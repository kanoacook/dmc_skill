# Ringprogress

**Component**: `dmc.Ringprogress`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify

dmc.Group(
    [
        dmc.RingProgress(
            id="ring-progress-label",
            sections=[{"value": 33, "color": "indigo"}],
            label=dmc.Text("33%", c="indigo", ta="center"),
        ),
        dmc.RingProgress(
            id="ring-progress-label2",
            sections=[
                {"value": 25, "color": "indigo"},
                {"value": 15, "color": "orange"},
            ],
            label=dmc.Text("App data usage", size="xs", ta="center"),
        ),
        dmc.RingProgress(
            id="ring-progress-label3",
            sections=[{"value": 60, "color": "green"}, {"value": 5, "color": "yellow"}],
            label=dmc.Center(
                dmc.ActionIcon(
                    color="teal",
                    variant="light",
                    radius="xl",
                    size="xl",
                    children=DashIconify(icon="tabler:check", height=40),
                )
            ),
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
