# Sparkline

**Component**: `dmc.Sparkline`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
areaProps, color, connectNulls, curveType, data, fillOpacity, strokeWidth, trendColors, withGradient
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `areaProps` | ? | See all-components.md for details |
| `color` | ? | See all-components.md for details |
| `connectNulls` | ? | See all-components.md for details |
| `curveType` | ? | See all-components.md for details |
| `data` | ? | See all-components.md for details |
| `fillOpacity` | ? | See all-components.md for details |
| `strokeWidth` | ? | See all-components.md for details |
| `trendColors` | ? | See all-components.md for details |
| `withGradient` | ? | See all-components.md for details |


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

dmc.Sparkline(
    id="my-sparkline",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
