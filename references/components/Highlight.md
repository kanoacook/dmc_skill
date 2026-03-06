# Highlight

**Component**: `dmc.Highlight`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Highlight(
    "You can change styles of highlighted part if you do not like default styles",
    ta="center",
    highlight=["highlighted", "default"],
    highlightStyles={
        "backgroundImage": "linear-gradient(45deg, var(--mantine-color-cyan-5), var(--mantine-color-indigo-5))",
        "fontWeight": 500,
        "WebkitBackgroundClip": "text",
        "WebkitTextFillColor": "transparent",
    },
)

---

## Props

The following props are specific to this component:

```
children, color, gradient, highlight, highlightStyles, inherit, inline, lineClamp, size, span, truncate
```

**Props count**: 11

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
