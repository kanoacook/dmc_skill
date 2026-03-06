# Hovercard

**Component**: `dmc.Hovercard`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify

(
    dmc.HoverCard(
        shadow="md",
        children=[
            dmc.HoverCardTarget(
                dmc.Avatar(
                    src="https://avatars.githubusercontent.com/u/91216500?v=4",
                    radius="xl",
                )
            ),
            dmc.HoverCardDropdown(
                [
                    dmc.Button(
                        "Snehil Vijay", fullWidth=True, mb=15, variant="outline"
                    ),
                    dmc.Group(
                        [
                            dmc.Anchor(
                                DashIconify(icon="logos:linkedin-icon", width=30),
                                href="https://www.linkedin.com/in/snehilvj/",
                                target="_blank",
                            ),
                            dmc.Anchor(
                                DashIconify(icon="logos:github-octocat", width=30),
                                href="https://www.github.com/snehilvj/",
                                target="_blank",
                            ),
                            dmc.Anchor(
                                DashIconify(icon="logos:twitter", width=30),
                                href="https://twitter.com/snehilvj",
                                target="_blank",
                            ),
                        ],
                        p=0,
                    ),
                ]
            ),
        ],
    ),
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
