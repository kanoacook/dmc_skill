# Navlink

**Component**: `dmc.Navlink`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html
from dash_iconify import DashIconify


def get_icon(icon):
    return DashIconify(icon=icon, height=16)


html.Div(
    [
        dmc.NavLink(
            label="With icon",
            leftSection=get_icon(icon="bi:house-door-fill"),
        ),
        dmc.NavLink(
            label="With right section",
            leftSection=get_icon(icon="tabler:gauge"),
            rightSection=get_icon(icon="tabler-chevron-right"),
        ),
        dmc.NavLink(
            label="Disabled",
            leftSection=get_icon(icon="tabler:circle-off"),
            disabled=True,
        ),
        dmc.NavLink(
            label="With description",
            description="Additional information",
            leftSection=dmc.Badge(
                "3", size="xs", variant="filled", color="red", w=16, h=16, p=0
            ),
        ),
        dmc.NavLink(
            label="Active subtle",
            leftSection=get_icon(icon="tabler:activity"),
            rightSection=get_icon(icon="tabler-chevron-right"),
            variant="subtle",
            active=True,
        ),
        dmc.NavLink(
            label="Active light",
            leftSection=get_icon(icon="tabler:activity"),
            rightSection=get_icon(icon="tabler-chevron-right"),
            active=True,
        ),
        dmc.NavLink(
            label="Active filled",
            leftSection=get_icon(icon="tabler:activity"),
            rightSection=get_icon(icon="tabler-chevron-right"),
            variant="filled",
            active=True,
        ),
    ],
    style={"width": 240},
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
