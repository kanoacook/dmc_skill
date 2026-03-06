# Button

**Component**: `dmc.Button`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify
from dash import html

icon = DashIconify(icon="tabler:photo", width=14)

component = dmc.Stack(
    [
        dmc.Button(
            "Button label",
            justify="center",
            fullWidth=True,
            leftSection=icon,
            rightSection=icon,
            variant="default",
        ),
        dmc.Button(
            "Button label",
            justify="center",
            fullWidth=True,
            leftSection=icon,
            variant="default",
            mt="md",
        ),
        dmc.Button(
            "Button label",
            justify="center",
            fullWidth=True,
            rightSection=icon,
            variant="default",
            mt="md",
        ),
        dmc.Button(
            "Button label",
            justify="center",
            fullWidth=True,
            leftSection=html.Span(),  # Empty spacer
            rightSection=icon,
            variant="default",
            mt="md",
        ),
    ]
)

---

## Props

The following props are specific to this component:

```
autoContrast, children, color, disabled, fullWidth, gradient, justify, leftSection, loaderProps, loading, n_clicks, radius, rightSection, size
```

**Props count**: 14

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
