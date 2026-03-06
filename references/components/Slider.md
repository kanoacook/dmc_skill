# Slider

**Component**: `dmc.Slider`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

marks = [
    {"value": 0, "label": "xs"},
    {"value": 25, "label": "sm"},
    {"value": 50, "label": "md"},
    {"value": 75, "label": "lg"},
    {"value": 100, "label": "xl"},
]

component = dmc.Container([
    dmc.Text("Decimal step"),
    dmc.Slider(
        value=0,
        min=-10,
        max=10,
        step=0.1,
        label={"function": "formatDecimal"},
        styles={"markLabel": {"display": "none"}},
    ),

    dmc.Text("Step matched with marks", mt="md"),
    dmc.Slider(
        value=50,
        step=25,
        marks=marks,
        label={"function": "labelFromMarks", "options": {"marks": marks}},
        styles={"markLabel": {"display": "none"}},
    ),
], p="xl")

---

## Props

The following props are specific to this component:

```
color, disabled, domain, inverted, label, labelAlwaysOn, labelTransitionProps, marks, max, min, name, persisted_props, persistence, persistence_type, precision, radius, restrictToMarks, scale, showLabelOnHover, size, step, thumbChildren, thumbLabel, thumbSize, updatemode, value
```

**Props count**: 26

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
