# Drawer

**Component**: `dmc.Drawer`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
children, closeButtonProps, closeOnClickOutside, closeOnEscape, keepMounted, lockScroll, offset, opened, overlayProps, padding, portalProps, position, radius, removeScrollProps, returnFocus, shadow, size, title, transitionProps, trapFocus, withCloseButton, withOverlay, withinPortal, zIndex
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `children` | ? | See all-components.md for details |
| `closeButtonProps` | ? | See all-components.md for details |
| `closeOnClickOutside` | ? | See all-components.md for details |
| `closeOnEscape` | ? | See all-components.md for details |
| `keepMounted` | ? | See all-components.md for details |
| `lockScroll` | ? | See all-components.md for details |
| `offset` | ? | See all-components.md for details |
| `opened` | ? | See all-components.md for details |
| `overlayProps` | ? | See all-components.md for details |
| `padding` | ? | See all-components.md for details |
| `portalProps` | ? | See all-components.md for details |
| `position` | ? | See all-components.md for details |
| `radius` | ? | See all-components.md for details |
| `removeScrollProps` | ? | See all-components.md for details |
| `returnFocus` | ? | See all-components.md for details |
| `shadow` | ? | See all-components.md for details |
| `size` | ? | See all-components.md for details |
| `title` | ? | See all-components.md for details |
| `transitionProps` | ? | See all-components.md for details |
| `trapFocus` | ? | See all-components.md for details |
| `withCloseButton` | ? | See all-components.md for details |
| `withOverlay` | ? | See all-components.md for details |
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

dmc.Drawer(
    id="my-drawer",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
