# Actionicon

**Component**: `dmc.Actionicon`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify
from dash import callback, Input, Output

dmc.Box([
    dmc.Group(
        [
            dmc.ActionIcon(
                id="icon-loading-default",
                children=DashIconify(icon="tabler:heart", width=18, height=18)
            ),
            dmc.ActionIcon(
                id="icon-loading-light",
                children=DashIconify(icon="tabler:heart", width=18, height=18),
                variant="light",
            ),
            dmc.ActionIcon(
                id="icon-loading-outline",
                children=DashIconify(icon="tabler:heart", width=18, height=18),
                variant="outline",
            ),
        ]
    ),
    dmc.Switch(
        id="loading-switch",
        label="Loading state",
        checked=False,
        mt="md",
    ),
])


@callback(
    Output("icon-loading-default", "loading"),
    Output("icon-loading-light", "loading"),
    Output("icon-loading-outline", "loading"),
    Input("loading-switch", "checked"),
)
def toggle_loading(loading_state):
    return loading_state, loading_state, loading_state

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
