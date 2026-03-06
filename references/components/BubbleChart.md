# BubbleChart

**Component**: `dmc.BubbleChart`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
clickData, color, data, dataKey, gridColor, hoverData, label, range, scatterProps, textColor, tooltipProps, valueFormatter, withTooltip, xAxisProps, yAxisProps, zAxisProps
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `clickData` | ? | See all-components.md for details |
| `color` | ? | See all-components.md for details |
| `data` | ? | See all-components.md for details |
| `dataKey` | ? | See all-components.md for details |
| `gridColor` | ? | See all-components.md for details |
| `hoverData` | ? | See all-components.md for details |
| `label` | ? | See all-components.md for details |
| `range` | ? | See all-components.md for details |
| `scatterProps` | ? | See all-components.md for details |
| `textColor` | ? | See all-components.md for details |
| `tooltipProps` | ? | See all-components.md for details |
| `valueFormatter` | ? | See all-components.md for details |
| `withTooltip` | ? | See all-components.md for details |
| `xAxisProps` | ? | See all-components.md for details |
| `yAxisProps` | ? | See all-components.md for details |
| `zAxisProps` | ? | See all-components.md for details |


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

dmc.BubbleChart(
    id="my-bubblechart",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
