# Inputwrapper

**Component**: `dmc.Inputwrapper`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

from dash import Input, Output, callback


 dmc.InputWrapper(
    id="tree-wrapper",
    label="Tree input",
    description="This is a tree input",
    inputWrapperOrder=["label", "description", "error", "input"],
    withAsterisk=True,
    children=[
        dmc.Tree(
            id="tree",
            checkboxes=True,
            data=[
                {
                    "label": "root",
                    "value": "value",
                    "children": [
                        {"label": "child 1", "value": "child_1"},
                        {"label": "child 2", "value": "child_2"},
                    ],
                }
            ],
        )
    ],
)

@callback(
    Output("tree-wrapper", "error"),
    Input("tree", "checked"),
)
def validate(checked):
    tree_error = "Select at least one" if not checked else None
    return tree_error

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
