# Textarea

**Component**: `dmc.Textarea`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

dmc.Stack(
    children=[
        dmc.Textarea(
            label="Autosize with no rows limit",
            placeholder="Autosize with no rows limit",
            w=500,
            autosize=True,
            minRows=2,
        ),
        dmc.Textarea(
            label="Autosize with 4 rows max",
            placeholder="Autosize with 4 rows max",
            w=500,
            autosize=True,
            minRows=2,
            maxRows=4,
        ),
    ],
)

---

## Props

The following props are specific to this component:

```
autoComplete, autosize, debounce, description, descriptionProps, disabled, error, errorProps, inputProps, inputWrapperOrder, label, labelProps, leftSection, leftSectionPointerEvents, leftSectionProps, leftSectionWidth, maxRows, minRows, n_blur, n_submit, name, persisted_props, persistence, persistence_type, placeholder, pointer, radius, readOnly, required, resize, rightSection, rightSectionPointerEvents, rightSectionProps, rightSectionWidth, size, spellCheck, value, withAsterisk, withErrorStyles, wrapperProps
```

**Props count**: 40

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
