# Avatar

**Component**: `dmc.Avatar`

**Version**: 2.6.0

---

## Overview

from os import environ

import dash_mantine_components as dmc
import requests


def create_contributors_list():
    resp = requests.get(
        "https://api.github.com/repos/snehilvj/dash-mantine-components/contributors",
        headers={"authorization": f"token {environ['CONTRIB_TOKEN']}"},
    )
    contributors = resp.json()

    children = []
    for user in contributors:
        avatar = dmc.Avatar(src=user["avatar_url"], radius="xl")
        children.append(avatar)

    return dmc.AvatarGroup(children, id="avatar-group")


create_contributors_list() if "CONTRIB_TOKEN" in environ else None

---

## Props

The following props are specific to this component:

```
allowedInitialsColors, alt, autoContrast, children, color, gradient, imageProps, name, radius, size, src
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
