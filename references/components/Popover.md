# Popover

**Component**: `dmc.Popover`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc


dmc.Box(
    style={"border": "1px solid var(--mantine-color-dimmed)", "overflow": "auto"},
    p="xl",
    w=400,
    h=200,
    children=[
        dmc.Box(
            w=1000,
            h=400,
            children=dmc.Group(
                [
                    dmc.Popover(
                        opened=True,
                        width="target",
                        position="bottom",
                        closeOnClickOutside=False,
                        children=[
                            dmc.PopoverTarget(
                                dmc.Button("Toggle popover")
                            ),
                            dmc.PopoverDropdown("This popover dropdown is hidden when detached"),
                        ],
                    ),
                    dmc.Popover(
                        opened=True,
                        width="target",
                        position="bottom",
                        closeOnClickOutside=False,
                        hideDetached=False,
                        children=[
                            dmc.PopoverTarget(
                                dmc.Button("Toggle popover")
                            ),
                            dmc.PopoverDropdown("This popover dropdown is visible when detached"),
                        ],
                    ),
                ]
            ),
        )
    ]
)

---

## Props

The following props are specific to this component:

```
arrowOffset, arrowPosition, arrowRadius, arrowSize, children, clickOutsideEvents, closeOnClickOutside, closeOnEscape, disabled, floatingStrategy, hideDetached, keepMounted, middlewares, offset, opened, overlayProps, portalProps, position, positionDependencies, radius, returnFocus, shadow, transitionProps, trapFocus, width, withArrow, withOverlay, withRoles, withinPortal, zIndex
```

**Props count**: 30

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
