# Tabs

**Component**: `dmc.Tabs`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import Input, Output, html, callback

from lib.utils import create_graph

html.Div(
    [
        dmc.Tabs(
            [
                dmc.TabsList(
                    [
                        dmc.TabsTab("Tab one", value="1"),
                        dmc.TabsTab("Tab two", value="2"),
                    ]
                ),
            ],
            id="tabs-example",
            value="1",
        ),
        html.Div(id="tabs-content", style={"paddingTop": 10}),
    ]
)


@callback(Output("tabs-content", "children"), Input("tabs-example", "value"))
def render_content(active):
    if active == "1":
        return [dmc.Text("Tab One selected", my=10), create_graph()]
    else:
        return [dmc.Text("Tab Two selected", my=10), create_graph()]

---

## Props

The following props are specific to this component:

```
activateTabWithKeyboard, allowTabDeactivation, autoContrast, children, color, inverted, keepMounted, loop, orientation, persisted_props, persistence, persistence_type, placement, radius, value
```

**Props count**: 15

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
