# Autocomplete

**Component**: `dmc.Autocomplete`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc
from dash import Output, Input, html, callback

html.Div(
    [
        dmc.Button("Toggle dropdown", id="btn-autocomplete-opened", n_clicks=0),
        dmc.Autocomplete(
            label="Select your favorite library",
            placeholder="Select value",
            id="autocomplete-opened",
            data=["Pandas", "NumPy", "TensorFlow", "PyTorch"],
            comboboxProps={"position": "bottom", "middlewares": {"flip": False, "shift": False}},
            mb=10,
        ),
    ]
)


@callback(
    Output("autocomplete-opened", "dropdownOpened"), Input("btn-autocomplete-opened", "n_clicks")
)
def select_value(n):
    if n % 2 == 0:
        return False
    return True

---

## Props

The following props are specific to this component:

```
autoSelectOnBlur, clearButtonProps, clearable, comboboxProps, data, debounce, description, descriptionProps, disabled, dropdownOpened, error, errorProps, filter, inputProps, inputWrapperOrder, label, labelProps, leftSection, leftSectionPointerEvents, leftSectionProps, leftSectionWidth, limit, maxDropdownHeight, n_blur, n_submit, name, persisted_props, persistence, persistence_type, placeholder, pointer, radius, readOnly, renderOption, required, rightSection, rightSectionPointerEvents, rightSectionProps, rightSectionWidth, scrollAreaProps, selectFirstOptionOnChange, size, value, withAsterisk, withErrorStyles, withScrollArea, wrapperProps
```

**Props count**: 47

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
