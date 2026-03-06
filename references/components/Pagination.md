# Pagination

**Component**: `dmc.Pagination`

**Version**: 2.6.0

---

## Overview

from dash import  html, Output, Input, callback
import dash_mantine_components as dmc


limit = 10
total = 145
total_pages = (total + limit - 1) // limit

dmc.Group(
    justify="flex-end",
    children=[
        dmc.Text(id="message-withPages", size="sm"),
        dmc.Pagination(id="pagination-withPages", total=total_pages, value=1, withPages=False),
    ],
)


@callback(
    Output("message-withPages", "children"),
    Input("pagination-withPages", "value"),
)
def update_message(page):
    start = limit * (page - 1) + 1
    end = min(total, limit * page)
    return f"Showing {start} – {end} of {total}"

---

## Props

The following props are specific to this component:

```
autoContrast, boundaries, color, disabled, gap, hideWithOnePage, persisted_props, persistence, persistence_type, radius, siblings, size, total, value, withControls, withEdges, withPages
```

**Props count**: 17

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
