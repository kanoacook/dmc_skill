# Accordion

**Component**: `dmc.Accordion`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
chevron, chevronIconSize, chevronPosition, chevronSize, children, disableChevronRotation, loop, multiple, order, persisted_props, persistence, persistence_type, radius, transitionDuration, value
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `chevron` | ? | See all-components.md for details |
| `chevronIconSize` | ? | See all-components.md for details |
| `chevronPosition` | ? | See all-components.md for details |
| `chevronSize` | ? | See all-components.md for details |
| `children` | ? | See all-components.md for details |
| `disableChevronRotation` | ? | See all-components.md for details |
| `loop` | ? | See all-components.md for details |
| `multiple` | ? | See all-components.md for details |
| `order` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `radius` | ? | See all-components.md for details |
| `transitionDuration` | ? | See all-components.md for details |
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

dmc.Accordion(
    id="my-accordion",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
