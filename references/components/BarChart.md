# Barchart

**Component**: `dmc.Barchart`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html, dcc
from .data import data

# Define patterns for custom colors
pattern_definitions = dcc.Markdown('''
<svg>
  <defs>
    <pattern id="diagonalStripes" patternUnits="userSpaceOnUse" width="6" height="8" patternTransform="rotate(45)">
      <rect width="2" height="8" fill="rgba(0, 128, 128, 0.7)"></rect>
    </pattern>
    <pattern id="crosshatch" patternUnits="userSpaceOnUse" width="8" height="8">
      <path d="M 0 0 L 8 0 L 8 8 L 0 8 Z" fill="none" stroke="rgba(75, 0, 130, 0.7)" strokeWidth="1"></path>
      <path d="M 0 0 L 8 8" stroke="rgba(75, 0, 130, 0.7)" strokeWidth="1"></path>
      <path d="M 8 0 L 0 8" stroke="rgba(75, 0, 130, 0.7)" strokeWidth="1"></path>
    </pattern>
  </defs>
</svg>
''', dangerously_allow_html=True)

html.Div([
    pattern_definitions,
    dmc.BarChart(
        h=300,
        dataKey="month",
        data=data,
        type="stacked",
        series=[
            {"name": "Smartphones", "color": "url(#crosshatch)"},
            {"name": "Laptops", "color": "blue.6"},
            {"name": "Tablets", "color": "url(#diagonalStripes)"},
        ],
    )
])

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
