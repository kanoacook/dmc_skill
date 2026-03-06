# Switch

**Component**: `dmc.Switch`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html, Output, Input, callback

html.Div(
    [
        dmc.Switch(id="switch-example", label="Use default settings.", checked=True),
        dmc.Space(h=10),
        dmc.Text(id="switch-settings"),
    ]
)


@callback(Output("switch-settings", "children"), Input("switch-example", "checked"))
def settings(checked):
    return f"Using {'default' if checked else 'custom'} settings"

---

## Props

The following props are specific to this component:

```
checked, color, description, disabled, error, label, labelPosition, offLabel, onLabel, persisted_props, persistence, persistence_type, radius, size, thumbIcon, withThumbIndicator, wrapperProps
```

**Props count**: 17

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
