# Slider

**Component**: `dmc.Slider`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
color, disabled, domain, inverted, label, labelAlwaysOn, labelTransitionProps, marks, max, min, name, persisted_props, persistence, persistence_type, precision, radius, restrictToMarks, scale, showLabelOnHover, size, step, thumbChildren, thumbLabel, thumbSize, updatemode, value
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `color` | ? | See all-components.md for details |
| `disabled` | ? | See all-components.md for details |
| `domain` | ? | See all-components.md for details |
| `inverted` | ? | See all-components.md for details |
| `label` | ? | See all-components.md for details |
| `labelAlwaysOn` | ? | See all-components.md for details |
| `labelTransitionProps` | ? | See all-components.md for details |
| `marks` | ? | See all-components.md for details |
| `max` | ? | See all-components.md for details |
| `min` | ? | See all-components.md for details |
| `name` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `precision` | ? | See all-components.md for details |
| `radius` | ? | See all-components.md for details |
| `restrictToMarks` | ? | See all-components.md for details |
| `scale` | ? | See all-components.md for details |
| `showLabelOnHover` | ? | See all-components.md for details |
| `size` | ? | See all-components.md for details |
| `step` | ? | See all-components.md for details |
| `thumbChildren` | ? | See all-components.md for details |
| `thumbLabel` | ? | See all-components.md for details |
| `thumbSize` | ? | See all-components.md for details |
| `updatemode` | ? | See all-components.md for details |
| `value` | ? | See all-components.md for details |


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

dmc.Slider(
    id="my-slider",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
