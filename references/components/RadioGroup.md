# Radiogroup

**Component**: `dmc.Radiogroup`

**Version**: 2.6.0

---

## Overview

from dash import  Input, Output, callback
import dash_mantine_components as dmc

def make_radiocard(label, description):
    return dmc.RadioCard(
        withBorder=True,
        p="md",
        mt="md",
        className="checkboxcard-root",
        value=label,
        children=[
            dmc.Group([
                dmc.RadioIndicator(),
                dmc.Box([
                    dmc.Text(label, lh="1.3", fz="md", fw="bold" ),
                    dmc.Text(description, size="sm", c="dimmed"),
                ])
            ], wrap="nowrap", align="flex-start"),
        ]
    )


component = dmc.Box([
    dmc.RadioGroup(
        id="radiocard-group",
        label= "RadioGroup label",
        value="RadioCard 1",
        description="This is a RadioGroup description",
        deselectable=True,
        children=[
            make_radiocard(f"RadioCard {i}", f"RadioCard description {i}")
            for i in range(1, 5)
        ]
    ),
    dmc.Box(id="radio-group-out"),
])


@callback(
    Output("radiocard-group-out", "children"),
    Input("radiocard-group", "value")
)
def update(checked):
   return f"Selected: {checked}"

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
