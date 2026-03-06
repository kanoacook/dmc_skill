# Group

**Component**: `dmc.Group`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Box(
    style={"overflow": "hidden"},
    children=[
        dmc.Box(
            maw=500,
            p="md",
            mx="auto",
            bg="var(--mantine-color-blue-light)",
            children=[
                dmc.Text(
                    size="sm",
                    mb=5,
                    children=(
                        "preventGrowOverflow: true – each child width is always limited "
                        "to 33% of parent width (since there are 3 children)"
                    ),
                ),
                dmc.Group(
                    grow=True,
                    wrap="nowrap",
                    children=[
                        dmc.Button("First button", variant="default"),
                        dmc.Button("Second button with large content", variant="default"),
                        dmc.Button("Third button", variant="default"),
                    ],
                ),
                dmc.Text(
                    size="sm",
                    mb=5,
                    mt="md",
                    children=(
                        "preventGrowOverflow: false – children will grow based on their "
                        "content, they can take more than 33% of parent width"
                    ),
                ),
                dmc.Group(
                    grow=True,
                    preventGrowOverflow=False,
                    wrap="nowrap",
                    children=[
                        dmc.Button("First button", variant="default"),
                        dmc.Button("Second button with large content", variant="default"),
                        dmc.Button("Third button", variant="default"),
                    ],
                ),
            ],
        )
    ],
)

---

## Props

The following props are specific to this component:

```
align, children, gap, grow, justify, preventGrowOverflow, wrap
```

**Props count**: 7

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
