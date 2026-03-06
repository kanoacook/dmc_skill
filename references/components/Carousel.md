# Carousel

**Component**: `dmc.Carousel`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
active, autoScroll, autoplay, children, controlSize, controlsOffset, emblaOptions, height, includeGapInSize, initialSlide, nextControlIcon, orientation, previousControlIcon, slideGap, slideSize, type, withControls, withIndicators, withKeyboardEvents
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `active` | ? | See all-components.md for details |
| `autoScroll` | ? | See all-components.md for details |
| `autoplay` | ? | See all-components.md for details |
| `children` | ? | See all-components.md for details |
| `controlSize` | ? | See all-components.md for details |
| `controlsOffset` | ? | See all-components.md for details |
| `emblaOptions` | ? | See all-components.md for details |
| `height` | ? | See all-components.md for details |
| `includeGapInSize` | ? | See all-components.md for details |
| `initialSlide` | ? | See all-components.md for details |
| `nextControlIcon` | ? | See all-components.md for details |
| `orientation` | ? | See all-components.md for details |
| `previousControlIcon` | ? | See all-components.md for details |
| `slideGap` | ? | See all-components.md for details |
| `slideSize` | ? | See all-components.md for details |
| `type` | ? | See all-components.md for details |
| `withControls` | ? | See all-components.md for details |
| `withIndicators` | ? | See all-components.md for details |
| `withKeyboardEvents` | ? | See all-components.md for details |


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

dmc.Carousel(
    id="my-carousel",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
