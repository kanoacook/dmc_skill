# Card

**Component**: `dmc.Card`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash_iconify import DashIconify

urls = [
    "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/images/bg-1.png",
    "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/images/bg-2.png",
    "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/images/bg-3.png",
]

images = [dmc.Image(radius="sm", src=url) for url in urls]

dmc.Card(
    children=[
        dmc.CardSection(
            dmc.Group(
                children=[
                    dmc.Text("Review Pictures", fw=500),
                    dmc.ActionIcon(
                        DashIconify(icon="carbon:overflow-menu-horizontal"),
                        color="gray",
                        variant="transparent",
                    ),
                ],
                justify="space-between",
            ),
            withBorder=True,
            inheritPadding=True,
            py="xs",
        ),
        dmc.Text(
            children=[
                dmc.Text(
                    "200+ images uploaded",
                    c="blue",
                    style={"display": "inline"},
                ),
                " since last visit, review them to select which one should be added to your gallery",
            ],
            mt="sm",
            c="dimmed",
            size="sm",
        ),
        dmc.CardSection(
            dmc.Image(
                src="https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/images/bg-4.png",
                mt="sm",
            ),
        ),
        dmc.CardSection(
            children=[
                dmc.SimpleGrid(cols=3, children=[i for i in images]),
            ],
            inheritPadding=True,
            mt="sm",
            pb="md",
        ),
    ],
    withBorder=True,
    shadow="sm",
    radius="md",
    w=350,
)

---

## Props

The following props are specific to this component:

```
children, padding, radius, shadow, withBorder
```

**Props count**: 5

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
