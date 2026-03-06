# Tooltip

**Component**: `dmc.Tooltip`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Center(
    [
        dmc.FloatingTooltip(
            label="Tooltip",
            color="orange",
            children=[
                dmc.Center(
                    dmc.Text("Hover over the box to see tooltip"),
                    style={
                        "height": 100,
                        "padding": 10,
                        "border": "2px solid  var(--mantine-color-gray-6)",
                    },
                )
            ],
        )
    ]
)

---

## Props

The following props are specific to this component:

```
arrowOffset, arrowPosition, arrowRadius, arrowSize, autoContrast, boxWrapperProps, children, closeDelay, color, disabled, events, floatingStrategy, inline, keepMounted, label, middlewares, multiline, offset, openDelay, opened, portalProps, position, positionDependencies, radius, target, transitionProps, withArrow, withinPortal, zIndex
```

**Props count**: 29

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
