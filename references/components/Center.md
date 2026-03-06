# Center

**Component**: `dmc.Center`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify

dmc.Box(
    dmc.Anchor(
        href="https://mantine.dev",
        target="_blank",
        children=dmc.Center(
            [
                DashIconify(
                    icon="tabler:arrow-left",  # Use the Tabler Arrow Left icon
                    width=12,
                    height=12,
                ),
                dmc.Box("Back to Mantine website", ml=5),
            ],
            inline=True,
        ),
    )
)

---

## Props

The following props are specific to this component:

```
children, inline
```

**Props count**: 2

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
