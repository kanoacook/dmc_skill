# Datepickerinput

**Component**: `dmc.Datepickerinput`

**Version**: 2.6.0

---

## Overview

from datetime import date, timedelta
from dateutil.relativedelta import relativedelta
import dash_mantine_components as dmc


today = date.today()

dmc.DatePickerInput(
    type="range",
    label="With presets",
    placeholder="Select date",
    presets=[
        {
            "value": [
                (today - timedelta(days=2)).isoformat(),
                today.isoformat(),
            ],
            "label": "Last two days",
        },
        {
            "value": [
                (today - timedelta(days=7)).isoformat(),
                today.isoformat(),
            ],
            "label": "Last 7 days",
        },
        {
            "value": [
                today.replace(day=1).isoformat(),
                today.isoformat(),
            ],
            "label": "This month",
        },
        {
            "value": [
                (today - relativedelta(months=1)).replace(day=1).isoformat(),
                (today.replace(day=1) - timedelta(days=1)).isoformat(),
            ],
            "label": "Last month",
        },
        {
            "value": [
                date(today.year - 1, 1, 1).isoformat(),
                date(today.year - 1, 12, 31).isoformat(),
            ],
            "label": "Last year",
        },
    ],
    maw=320
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
