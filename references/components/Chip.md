# Chip

**Component**: `dmc.Chip`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import callback, Input, Output

dmc.Box(
    [
        dmc.Group(
            dmc.ChipGroup(
                [
                    dmc.Chip("Single chip", value="a"),
                    dmc.Chip("Can be selected", value="b"),
                    dmc.Chip("At a time", value="c"),
                ],
                multiple=False,
                value="a",
                deselectable=True,
                id="chipgroup-deselect",
            ),
            justify="center",
        ),
        dmc.Text(id="chipgroup-deselect-container", ta="center"),
    ]
)


@callback(
    Output("chipgroup-deselect-container", "children"), Input("chipgroup-deselect", "value")
)
def checkbox(value):
    return f"You selected chip: {value}"

---

## Props

The following props are specific to this component:

```
autoContrast, checked, children, color, disabled, icon, persisted_props, persistence, persistence_type, radius, size, type, value, wrapperProps
```

**Props count**: 14

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
