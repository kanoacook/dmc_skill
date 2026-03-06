# Tree

**Component**: `dmc.Tree`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
allowRangeSelection, checkOnSpace, checkboxes, checked, clearSelectionOnOutsideClick, collapsedIcon, data, expandOnClick, expandOnSpace, expanded, expandedIcon, iconSide, levelOffset, renderNode, selectOnClick, selected
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `allowRangeSelection` | ? | See all-components.md for details |
| `checkOnSpace` | ? | See all-components.md for details |
| `checkboxes` | ? | See all-components.md for details |
| `checked` | ? | See all-components.md for details |
| `clearSelectionOnOutsideClick` | ? | See all-components.md for details |
| `collapsedIcon` | ? | See all-components.md for details |
| `data` | ? | See all-components.md for details |
| `expandOnClick` | ? | See all-components.md for details |
| `expandOnSpace` | ? | See all-components.md for details |
| `expanded` | ? | See all-components.md for details |
| `expandedIcon` | ? | See all-components.md for details |
| `iconSide` | ? | See all-components.md for details |
| `levelOffset` | ? | See all-components.md for details |
| `renderNode` | ? | See all-components.md for details |
| `selectOnClick` | ? | See all-components.md for details |
| `selected` | ? | See all-components.md for details |


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

dmc.Tree(
    id="my-tree",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
