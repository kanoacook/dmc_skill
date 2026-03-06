# Anchor

**Component**: `dmc.Anchor`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Group([
    dmc.Anchor(
        "Underline always",
        href="https://www.dash-mantine-components.com/",
        target="_blank",
        underline = "always",
    ),
    dmc.Anchor(
        "Underline on hover",
        href="https://www.dash-mantine-components.com/",
        target="_blank",
        underline = "hover",
    ),
    dmc.Anchor(
        "Underline never",
        href="https://www.dash-mantine-components.com/",
        target="_blank",
        underline = "never",
    ),
    dmc.Anchor(
        "Underline not hover",
        href="https://www.dash-mantine-components.com/",
        target="_blank",
        underline = "not-hover",
    ),

])

---

## Props

The following props are specific to this component:

```
children, gradient, href, inherit, inline, lineClamp, refresh, size, target, truncate, underline
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
