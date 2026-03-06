# Scrollarea

**Component**: `dmc.Scrollarea`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import callback, Input, Output, ctx


content = [
    dmc.Box([
        dmc.Title(f"Section {i}", order=4, mt="sm", id=f"section-{i}"),
        dmc.Text("""
            Lorem ipsum, dolor sit amet consectetur adipisicing elit.
            Dicta perspiciatis reiciendis voluptate eaque itaque quos.
            Natus iure tenetur libero, reprehenderit ad, sequi, in aliquam eos
            necessitatibus expedita delectus veniam culpa!            
        """)
    ])
    for i in range(1, 11)
]

dmc.Box([
    dmc.ScrollArea(
        content,
        id="scrollArea",
        h=250, w=350,
    ),
    dmc.Group([
        dmc.Button("Scroll to Top", id="scrollto-top"),
        dmc.Button("Scroll to Middle", id="scrollto-middle"),
        dmc.Button("Scroll to Bottom", id="scrollto-bottom"),
    ], mt="lg"),
])


@callback(
    Output("scrollArea", "scrollTo"),
    Input("scrollto-top", "n_clicks"),
    Input("scrollto-middle", "n_clicks"),
    Input("scrollto-bottom", "n_clicks"),
)
def scroll_to(t, m, b):
    if ctx.triggered_id == "scrollto-middle":
        return {"top": "50%"}
    if ctx.triggered_id == "scrollto-bottom":
        return {"top": "100%"}
    return {"top": 0}

---

## Props

The following props are specific to this component:

```
(See all-components.md for details)
```

**Props count**: 0

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
