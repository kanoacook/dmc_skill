# Menu

**Component**: `dmc.Menu`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc


menu = dmc.Menu(
    width=200,
    position="bottom-start",
    keepMounted=True, # required when using SubMenu
    children=[
        dmc.MenuTarget(
            dmc.Button("Toggle Menu")
        ),
        dmc.MenuDropdown([
            dmc.MenuItem("Dashboard"),

            dmc.SubMenu([
                dmc.SubMenuTarget(
                    dmc.SubMenuItem("Products")
                ),
                dmc.SubMenuDropdown([
                    dmc.MenuItem("All products"),
                    dmc.MenuItem("Categories"),
                    dmc.MenuItem("Tags"),
                    dmc.MenuItem("Attributes"),
                    dmc.MenuItem("Shipping classes"),
                ])
            ]),

            dmc.SubMenu([
                dmc.SubMenuTarget(
                    dmc.SubMenuItem("Orders")
                ),
                dmc.SubMenuDropdown([
                    dmc.MenuItem("Open"),
                    dmc.MenuItem("Completed"),
                    dmc.MenuItem("Cancelled"),
                ])
            ]),

            dmc.SubMenu([
                dmc.SubMenuTarget(
                    dmc.SubMenuItem("Settings")
                ),
                dmc.SubMenuDropdown([
                    dmc.MenuItem("Profile"),
                    dmc.MenuItem("Security"),
                    dmc.MenuItem("Notifications"),
                ])
            ]),
        ])
    ]
)

component=dmc.Center(menu)

---

## Props

The following props are specific to this component:

```
arrowOffset, arrowPosition, arrowRadius, arrowSize, children, clickOutsideEvents, closeDelay, closeOnClickOutside, closeOnEscape, closeOnItemClick, defaultOpened, disabled, floatingStrategy, keepMounted, loop, menuItemTabIndex, middlewares, offset, openDelay, opened, overlayProps, portalProps, position, positionDependencies, radius, returnFocus, shadow, transitionProps, trapFocus, trigger, width, withArrow, withOverlay, withinPortal, zIndex
```

**Props count**: 35

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
