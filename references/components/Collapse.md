# Collapse

**Component**: `dmc.Collapse`

**Version**: 2.6.0

---

## Overview

from dash import callback, Input, Output
import dash_mantine_components as dmc

dmc.Box([
    dmc.Button("Toggle Content", id="collapse-root-btn", n_clicks=0, mb="sm", size="lg"),
    dmc.Collapse(
        children=dmc.Box([
            dmc.Text("Hello World!", mt="lg"),
            dmc.Button(
                "Toggle Content",
                id="collapse-inner-btn",
                n_clicks=0,
                variant="outline",
                size="sm",
                my="lg",
                ml="lg"
            ),
            dmc.Collapse(children= dmc.Text("Hello Nested Worlds!", ml="lg"), id="collapse-inner")
        ]),
        opened=False,
        id="collapse-root"
    )
])

@callback(
    Output("collapse-root", "opened"),
    Input("collapse-root-btn", "n_clicks"),
)
def update(n):
    if n % 2 == 0:
        return False
    return True


@callback(
    Output("collapse-inner", "opened"),
    Input("collapse-inner-btn", "n_clicks"),
)
def update(n):
    if n % 2 == 0:
        return False
    return True

---

## Props

The following props are specific to this component:

```
animateOpacity, children, keepMounted, opened, transitionDuration, transitionTimingFunction
```

**Props count**: 6

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
