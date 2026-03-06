# List

**Component**: `dmc.List`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.List(
    [
        dmc.ListItem("First order item"),
        dmc.ListItem("First order item"),
        dmc.ListItem(
            [
                "First order item with list",
                dmc.List(
                    withPadding=True,
                    listStyleType="disc",
                    children=[
                        dmc.ListItem("Nested Item"),
                        dmc.ListItem("Nested Item"),
                        dmc.ListItem(
                            [
                                "Nested item with list",
                                dmc.List(
                                    withPadding=True,
                                    listStyleType="disc",
                                    children=[
                                        dmc.ListItem("Even more nested"),
                                        dmc.ListItem("Even more nested"),
                                    ],
                                ),
                            ]
                        ),
                        dmc.ListItem("Nested Item"),
                    ],
                ),
            ]
        ),
        dmc.ListItem("First order item"),
    ]
)

---

## Props

The following props are specific to this component:

```
center, children, icon, listStyleType, size, spacing, type, withPadding
```

**Props count**: 8

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
