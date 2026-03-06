# Checkbox

**Component**: `dmc.Checkbox`

**Version**: 2.6.0

---

## Overview

from dash import  html,  Input, Output,  callback, ALL, ctx
import dash_mantine_components as dmc

initial_values = [
    {"label": "Receive email notifications", "checked": False},
    {"label": "Receive sms notifications", "checked": True},
    {"label": "Receive push notifications", "checked": False},
]

html.Div([
    dmc.Checkbox(
        id="all-notifications",
        label="Receive all notifications",
        checked=False,
        indeterminate=False
    ),
    html.Div([
        dmc.Checkbox(
            id={"type": "notification-item", "index": i},
            label=item["label"],
            checked=item["checked"],
            style={"marginTop": "5px", "marginLeft": "33px"}
        )
        for i, item in enumerate(initial_values)
    ])
])



@callback(
    Output("all-notifications", "checked"),
    Output("all-notifications", "indeterminate"),
    Output({"type": "notification-item", "index": ALL}, "checked"),
    Input("all-notifications", "checked"),
    Input({"type": "notification-item", "index": ALL}, "checked"),
    prevent_initial_callback=True
)
def update_main_checkbox(all_checked, checked_states):
    # handle "all" checkbox"
    if ctx.triggered_id == 'all-notifications':
        checked_states = [all_checked] * len(checked_states)

    # handled individual check boxes
    all_checked_states = all(checked_states)
    indeterminate = any(checked_states) and not all_checked_states
    return all_checked_states, indeterminate, checked_states

---

## Props

The following props are specific to this component:

```
autoContrast, checked, color, description, disabled, error, icon, iconColor, indeterminate, indeterminateIcon, label, labelPosition, persisted_props, persistence, persistence_type, radius, size, value, wrapperProps
```

**Props count**: 19

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
