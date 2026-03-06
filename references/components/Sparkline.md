# Sparkline

**Component**: `dmc.Sparkline`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import html

positive_trend = [10, 20, 40, 20, 40, 10, 50]
negative_trend = [50, 40, 20, 40, 20, 40, 10]
neutral_trend = [10, 20, 40, 20, 40, 10, 50, 5, 10]


def make_sparkline(trend):
    return dmc.Sparkline(
        w=200,
        h=60,
        data=trend,
        trendColors={"positive": "teal.6", "negative": "red.6", "neutral": "gray.5"},
        fillOpacity=0.2,
    )


dmc.Stack(
    [
        dmc.Text("Positive Trend"),
        make_sparkline(positive_trend),
        dmc.Text("Negative Trend", mt="md"),
        make_sparkline(negative_trend),
        dmc.Text("Neutral Trend", mt="md"),
        make_sparkline(neutral_trend),
    ],
    gap="md",
)

---

## Props

The following props are specific to this component:

```
areaProps, color, connectNulls, curveType, data, fillOpacity, strokeWidth, trendColors, withGradient
```

**Props count**: 9

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
