# Tagsinput

**Component**: `dmc.Tagsinput`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import Output, Input, html, callback

html.Div(
    [
        dmc.TagsInput(
            label="Value is accepted on blur",
            placeholder="Select all you like!",
            id="framework-tags-input1",
            value=["Pandas", "NumPy"],
            w=400,
            mb=10,
        ),
        dmc.Text(id="tags-input-value1", mb="xl"),
        dmc.TagsInput(
            label="Value IS NOT accepted on blur",
            placeholder="Select all you like!",
            id="framework-tags-input2",
            value=["Pandas", "NumPy"],
            acceptValueOnBlur=False,
            w=400,
            mb=10,
        ),
        dmc.Text(id="tags-input-value2"),
    ]
)


@callback(
    Output("tags-input-value1", "children"), Input("framework-tags-input1", "value")
)
def select_value(value):
    return f"You selected {value}"


@callback(
    Output("tags-input-value2", "children"), Input("framework-tags-input2", "value")
)
def select_value(value):
    return f"You selected {value}"

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
