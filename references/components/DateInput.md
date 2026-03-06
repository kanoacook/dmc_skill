# Dateinput

**Component**: `dmc.Dateinput`

**Version**: 2.6.0

---

## Overview

from datetime import datetime

import dash_mantine_components as dmc

dmc.Group(
    gap="xl",
    children=[
        dmc.DateInput(
            value=datetime.now().date(),
            valueFormat="ddd, MMM D YY",
            label="ddd, MMM D YY",
            w=250,
        ),
        dmc.DateInput(
            value=datetime.now().date(),
            valueFormat="MMMM DD, YY",
            label="MMMM DD, YY",
            w=250,
        ),
        dmc.DateInput(
            value=datetime.now().date(),
            valueFormat="DD-MM-YYYY",
            label="DD-MM-YYYY",
            w=250,
        ),
    ],
)

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
