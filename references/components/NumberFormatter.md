# NumberFormatter

**Component**: `dmc.NumberFormatter`

**Version**: 2.6.0

---

## Overview

from dash import html
import dash_mantine_components as dmc

html.Div([
    html.Div(["With prefix: ", dmc.NumberFormatter(value=100, prefix="$")]),
    html.Div(["With suffix: ", dmc.NumberFormatter(value=100, suffix=" RUB")]),
])

---

## Props

The following props are specific to this component:

```
allowNegative, decimalScale, decimalSeparator, fixedDecimalScale, prefix, suffix, thousandSeparator, thousandsGroupStyle, value
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
