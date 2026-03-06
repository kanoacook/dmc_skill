# Table

**Component**: `dmc.Table`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Table(
    withTableBorder=True,
    withColumnBorders=True,

    children=[
        dmc.TableThead(
            dmc.TableTr([
                dmc.TableTh("Day"),
                dmc.TableTh("Time"),
                dmc.TableTh("Topic"),
                dmc.TableTh("Action"),
            ])
        ),
        dmc.TableTbody([
            dmc.TableTr([
                dmc.TableTd("Monday", tableProps={"rowSpan": 2}),
                dmc.TableTd("9:00 - 10:00"),
                dmc.TableTd("Building Interactive Dashboards with Dash"),
                dmc.TableTd(dmc.Button("Details", size="xs", variant="light")),
            ]),
            dmc.TableTr([
                dmc.TableTd("10:15 - 11:00"),
                dmc.TableTd("Advanced Callbacks and App Structure"),
                dmc.TableTd(dmc.Button("Details", size="xs", variant="light")),
            ]),
            dmc.TableTr([
                dmc.TableTd("Tuesday", tableProps={"rowSpan": 2}),
                dmc.TableTd("9:00 - 10:00"),
                dmc.TableTd("Data Visualization with Plotly Express"),
                dmc.TableTd(dmc.Button("Details", size="xs", variant="light")),
            ]),
            dmc.TableTr([
                dmc.TableTd("10:15 - 11:00"),
                dmc.TableTd("Deploying Dash Apps to the Web"),
                dmc.TableTd(dmc.Button("Details", size="xs", variant="light")),
            ]),
        ])
    ]
)

---

## Props

The following props are specific to this component:

```
borderColor, captionSide, children, data, highlightOnHover, highlightOnHoverColor, horizontalSpacing, layout, stickyHeader, stickyHeaderOffset, striped, stripedColor, tabularNums, verticalSpacing, withColumnBorders, withRowBorders, withTableBorder
```

**Props count**: 17

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
