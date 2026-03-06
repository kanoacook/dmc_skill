# Datetimepicker

**Component**: `dmc.Datetimepicker`

**Version**: 2.6.0

---

## Overview

from datetime import datetime, timedelta
from dateutil.relativedelta import relativedelta
import dash_mantine_components as dmc


now = datetime.now()

dmc.DateTimePicker(
    label="Pick date and time",
    placeholder="Pick date and time",
    presets=[
        {
            "value": (now - timedelta(days=1)).isoformat(),
            "label": "Yesterday",
        },
        {
            "value": now.isoformat(),
            "label": "Today",
        },
        {
            "value": (now + timedelta(days=1)).isoformat(),
            "label": "Tomorrow",
        },
        {
            "value": (now + relativedelta(months=1)).isoformat(),
            "label": "Next month",
        },
        {
            "value": (now + relativedelta(years=1)).isoformat(),
            "label": "Next year",
        },
        {
            "value": (now - relativedelta(months=1)).isoformat(),
            "label": "Last month",
        },
        {
            "value": (now - relativedelta(years=1)).isoformat(),
            "label": "Last year",
        },
    ]
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
