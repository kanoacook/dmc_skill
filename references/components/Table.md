# Table

**Component**: `dmc.Table`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
borderColor, captionSide, children, data, highlightOnHover, highlightOnHoverColor, horizontalSpacing, layout, stickyHeader, stickyHeaderOffset, striped, stripedColor, tabularNums, verticalSpacing, withColumnBorders, withRowBorders, withTableBorder
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `borderColor` | ? | See all-components.md for details |
| `captionSide` | ? | See all-components.md for details |
| `children` | ? | See all-components.md for details |
| `data` | ? | See all-components.md for details |
| `highlightOnHover` | ? | See all-components.md for details |
| `highlightOnHoverColor` | ? | See all-components.md for details |
| `horizontalSpacing` | ? | See all-components.md for details |
| `layout` | ? | See all-components.md for details |
| `stickyHeader` | ? | See all-components.md for details |
| `stickyHeaderOffset` | ? | See all-components.md for details |
| `striped` | ? | See all-components.md for details |
| `stripedColor` | ? | See all-components.md for details |
| `tabularNums` | ? | See all-components.md for details |
| `verticalSpacing` | ? | See all-components.md for details |
| `withColumnBorders` | ? | See all-components.md for details |
| `withRowBorders` | ? | See all-components.md for details |
| `withTableBorder` | ? | See all-components.md for details |


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

dmc.Table(
    id="my-table",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
