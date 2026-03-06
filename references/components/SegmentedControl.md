# SegmentedControl

**Component**: `dmc.SegmentedControl`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
autoContrast, color, data, disabled, fullWidth, name, orientation, persisted_props, persistence, persistence_type, radius, readOnly, size, transitionDuration, transitionTimingFunction, value, withItemsBorders
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `autoContrast` | ? | See all-components.md for details |
| `color` | ? | See all-components.md for details |
| `data` | ? | See all-components.md for details |
| `disabled` | ? | See all-components.md for details |
| `fullWidth` | ? | See all-components.md for details |
| `name` | ? | See all-components.md for details |
| `orientation` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `radius` | ? | See all-components.md for details |
| `readOnly` | ? | See all-components.md for details |
| `size` | ? | See all-components.md for details |
| `transitionDuration` | ? | See all-components.md for details |
| `transitionTimingFunction` | ? | See all-components.md for details |
| `value` | ? | See all-components.md for details |
| `withItemsBorders` | ? | See all-components.md for details |


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

dmc.SegmentedControl(
    id="my-segmentedcontrol",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
