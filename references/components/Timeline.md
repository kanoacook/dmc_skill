# Timeline

**Component**: `dmc.Timeline`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc


dmc.Timeline(
    active=1,
    bulletSize=15,
    lineWidth=2,
    children=[
        dmc.TimelineItem(
            title="New Branch",
            children=[
                dmc.Text(
                    [
                        "You've created new branch ",
                        dmc.Anchor("fix-notification", href="#", size="sm"),
                        " from master",
                    ],
                    c="dimmed",
                    size="sm",
                ),
            ],
        ),
        dmc.TimelineItem(
            title="Commits",
            children=[
                dmc.Text(
                    [
                        "You've pushed 23 commits to ",
                        dmc.Anchor("fix-notification", href="#", size="sm"),
                    ],
                    c="dimmed",
                    size="sm",
                ),
            ],
        ),
        dmc.TimelineItem(
            title="Pull Request",
            lineVariant="dashed",
            children=[
                dmc.Text(
                    [
                        "You've submitted a pull request ",
                        dmc.Anchor(
                            "Fix incorrect notification message (#178)",
                            href="#",
                            size="sm",
                        ),
                    ],
                    c="dimmed",
                    size="sm",
                ),
            ],
        ),
        dmc.TimelineItem(
            [
                dmc.Text(
                    [
                        dmc.Anchor(
                            "AnnMarieW",
                            href="https://github.com/AnnMarieW",
                            size="sm",
                        ),
                        " left a comment on your pull request",
                    ],
                    c="dimmed",
                    size="sm",
                ),
            ],
            title="Code Review",
        ),
    ],
)

---

## Props

The following props are specific to this component:

```
active, align, autoContrast, bulletSize, children, color, lineWidth, radius, reverseActive
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
