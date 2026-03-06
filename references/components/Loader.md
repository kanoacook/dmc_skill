# Loader

**Component**: `dmc.Loader`

**Version**: 2.6.0

---

## Overview

import time

import dash_mantine_components as dmc
from dash import html, Input, Output, callback

html.Div([
    dmc.Button("Compute", id="load-btn", loaderProps={"type": "dots"} ),
    dmc.Text(id="load-output"),
])


@callback(
    Output("load-output", "children"),
    Input("load-btn", "n_clicks"),
    running=[(Output("load-btn", "loading"), True, False)],
)
def long_compute(n):
    time.sleep(2)
    return "Done " + str(time.time())

---

## Props

The following props are specific to this component:

```
children, color, size, type
```

**Props count**: 4

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
