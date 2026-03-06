# Grid

**Component**: `dmc.Grid`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

style = {
    "border": f"1px solid var(--mantine-primary-color-filled)",
    "textAlign": "center",
}

dmc.Box(
    # Wrapper div is added for demonstration purposes only,
    # it is not required in real projects
    dmc.Grid(
        children=[
            dmc.GridCol(dmc.Box("1", style=style), span={"base": 12, "md": 6, "lg": 3}),
            dmc.GridCol(dmc.Box("2", style=style), span={"base": 12, "md": 6, "lg": 3}),
            dmc.GridCol(dmc.Box("3", style=style), span={"base": 12, "md": 6, "lg": 3}),
            dmc.GridCol(dmc.Box("4", style=style), span={"base": 12, "md": 6, "lg": 3}),
        ],
        gutter="xl",
        type="container",
        breakpoints={
            "xs": "100px",
            "sm": "200px",
            "md": "300px",
            "lg": "400px",
            "xl": "500px",
        },
    ),
    style={"resize": 'horizontal', "overflow": 'hidden', "maxWidth": '100%', "margin": 24 },
)

---

## Props

The following props are specific to this component:

```
align, breakpoints, children, columns, grow, gutter, justify, overflow, type
```

**Props count**: 9

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
