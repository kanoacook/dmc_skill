# Text

**Component**: `dmc.Text`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html

html.Div(
    [
        dmc.Text("Extra small text", size="xs"),
        dmc.Text("Small text", size="sm"),
        dmc.Text("Default text", size="md"),
        dmc.Text("Large text", size="lg"),
        dmc.Text("Extra large text", size="xl"),
        dmc.Text("Semi bold", fw=500),
        dmc.Text("Bold", fw=700),
        dmc.Text("Underlined", td="underline"),
        dmc.Text("Red text", c="red"),
        dmc.Text("Blue text", c="blue"),
        dmc.Text("Gray text", c="gray"),
        dmc.Text("Uppercase", tt="uppercase"),
        dmc.Text("capitalized text", tt="capitalize"),
        dmc.Text("Aligned to center", ta="center"),
        dmc.Text("Aligned to right", ta="right"),
    ]
)

---

## Props

The following props are specific to this component:

```
children, gradient, inherit, inline, lineClamp, size, span, truncate
```

**Props count**: 8

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
