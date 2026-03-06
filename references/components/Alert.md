# Alert

**Component**: `dmc.Alert`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html, Output, Input, State, callback

html.Div(
    [
        dmc.Alert(
            "Something terrible happened! You made a mistake and there is no going back, your data was lost forever! ",
            title="Bummer!",
            id="alert-dismiss",
            color="red",
            withCloseButton=True,
        ),
        dmc.Button("Toggle alert", id="alert-button", mt=20),
    ]
)


@callback(
    Output("alert-dismiss", "hide"),
    Input("alert-button", "n_clicks"),
    State("alert-dismiss", "hide"),
    prevent_initial_call=True,
)
def alert(n_clicks, hide):
    return not hide

---

## Props

The following props are specific to this component:

```
autoContrast, children, closeButtonLabel, color, duration, hide, icon, radius, title, withCloseButton
```

**Props count**: 10

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
