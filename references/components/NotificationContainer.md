# NotificationContainer

**Component**: `dmc.NotificationContainer`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
autoClose, clean, cleanQueue, containerWidth, hideNotifications, limit, notificationMaxHeight, portalProps, position, sendNotifications, transitionDuration, withinPortal, zIndex
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `autoClose` | ? | See all-components.md for details |
| `clean` | ? | See all-components.md for details |
| `cleanQueue` | ? | See all-components.md for details |
| `containerWidth` | ? | See all-components.md for details |
| `hideNotifications` | ? | See all-components.md for details |
| `limit` | ? | See all-components.md for details |
| `notificationMaxHeight` | ? | See all-components.md for details |
| `portalProps` | ? | See all-components.md for details |
| `position` | ? | See all-components.md for details |
| `sendNotifications` | ? | See all-components.md for details |
| `transitionDuration` | ? | See all-components.md for details |
| `withinPortal` | ? | See all-components.md for details |
| `zIndex` | ? | See all-components.md for details |


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

## Example Usage

```python
import dash_mantine_components as dmc

dmc.NotificationContainer(
    id="my-notificationcontainer",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
