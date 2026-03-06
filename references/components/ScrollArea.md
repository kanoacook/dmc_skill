# ScrollArea

**Component**: `dmc.ScrollArea`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
children, offsetScrollbars, overscrollBehavior, scrollHideDelay, scrollTo, scrollbarSize, scrollbars, type
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `children` | ? | See all-components.md for details |
| `offsetScrollbars` | ? | See all-components.md for details |
| `overscrollBehavior` | ? | See all-components.md for details |
| `scrollHideDelay` | ? | See all-components.md for details |
| `scrollTo` | ? | See all-components.md for details |
| `scrollbarSize` | ? | See all-components.md for details |
| `scrollbars` | ? | See all-components.md for details |
| `type` | ? | See all-components.md for details |


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

dmc.ScrollArea(
    id="my-scrollarea",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
