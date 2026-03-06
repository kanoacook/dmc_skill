# Progress

**Component**: `dmc.Progress`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc


dmc.Box(
    [
        dmc.ProgressRoot(
            [
                dmc.ProgressSection(
                    dmc.ProgressLabel("Documents"),
                    value=33,
                    color="cyan",
                    id="progress-section1",
                ),
                dmc.ProgressSection(
                    dmc.ProgressLabel("Photos"),
                    value=28,
                    color="pink",
                    id="progress-section2",
                ),
                dmc.ProgressSection(
                    dmc.ProgressLabel("Others"),
                    value=15,
                    color="orange",
                    id="progress-section3",
                ),
            ],
            size="40",
        ),
        dmc.Tooltip(
            target="#progress-section1",
            label="Documents – 33Gb",
        ),
        dmc.Tooltip(
            target="#progress-section2",
            label="Photos – 28Gb",
        ),
        dmc.Tooltip(
            target="#progress-section3",
            label="Other – 15Gb",
        ),
    ]
)

---

## Props

The following props are specific to this component:

```
animated, autoContrast, color, orientation, radius, size, striped, transitionDuration, value
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
