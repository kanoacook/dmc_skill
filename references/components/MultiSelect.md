# Multiselect

**Component**: `dmc.Multiselect`

**Version**: 2.6.0

---

## Overview

import dash_mantine_components as dmc

users_data = {
    "Emily Johnson": {
        "image": "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/avatars/avatar-7.png",
        "email": "emily92@gmail.com",
    },
    "Ava Rodriguez": {
        "image": "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/avatars/avatar-8.png",
        "email": "ava_rose@gmail.com",
    },
    "Olivia Chen": {
        "image": "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/avatars/avatar-4.png",
        "email": "livvy_globe@gmail.com",
    },
    "Ethan Barnes": {
        "image": "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/avatars/avatar-1.png",
        "email": "ethan_explorer@gmail.com",
    },
    "Mason Taylor": {
        "image": "https://raw.githubusercontent.com/mantinedev/mantine/master/.demo/avatars/avatar-2.png",
        "email": "mason_musician@gmail.com",
    },
}

component = dmc.MultiSelect(
    data=list(users_data.keys()),
    label="Employees of the month",
    placeholder="Search for employee",
    maxDropdownHeight=300,
    searchable=True,
    hidePickedOptions=True,
    renderOption={
        "function": "renderUserOption",
        "options": {"users": users_data},
    },
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
