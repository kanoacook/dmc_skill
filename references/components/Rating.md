# Rating

**Component**: `dmc.Rating`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc


dmc.Stack(
    [
        dmc.Group([dmc.Text("Fractions: 2"), dmc.Rating(fractions=2, value=1)]),
        dmc.Group([dmc.Text("Fractions: 3"), dmc.Rating(fractions=3, value=2.3333)]),
        dmc.Group([dmc.Text("Fractions: 4"), dmc.Rating(fractions=4, value=3.75)]),
    ]
)

---

## Props

The following props are specific to this component:

```
color, count, emptySymbol, fractions, fullSymbol, highlightSelectedOnly, name, persisted_props, persistence, persistence_type, readOnly, size, value
```

**Props count**: 13

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
