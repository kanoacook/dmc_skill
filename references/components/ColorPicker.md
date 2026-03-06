# Colorpicker

**Component**: `dmc.Colorpicker`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html, Input, Output, callback

html.Div(
    [
        dmc.Group(
            justify="space-between",
            children=[
                dmc.ColorPicker(id="colorpicker-format", format="hex", value="#343353"),
                dmc.Select(
                    id="format-select",
                    data=[
                        {"label": fmt.upper(), "value": fmt}
                        for fmt in ["hex", "hexa", "rgb", "rgba", "hsl", "hsla"]
                    ],
                    value="hex",
                ),
            ],
        ),
        dmc.Space(h=10),
        dmc.Text(id="selected-color-format"),
    ]
)


@callback(Output("colorpicker-format", "format"), Input("format-select", "value"))
def pick_format(value):
    return value


@callback(
    Output("selected-color-format", "children"), Input("colorpicker-format", "value")
)
def pick_color(color):
    return color

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
