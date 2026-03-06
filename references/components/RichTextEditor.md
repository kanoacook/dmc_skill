# RichTextEditor

**Component**: `dmc.RichTextEditor`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
debounce, editable, extensions, focus, html, json, labels, n_blur, persisted_props, persistence, persistence_type, selected, toolbar, withCodeHighlightStyles, withTypographyStyles
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `debounce` | ? | See all-components.md for details |
| `editable` | ? | See all-components.md for details |
| `extensions` | ? | See all-components.md for details |
| `focus` | ? | See all-components.md for details |
| `html` | ? | See all-components.md for details |
| `json` | ? | See all-components.md for details |
| `labels` | ? | See all-components.md for details |
| `n_blur` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `selected` | ? | See all-components.md for details |
| `toolbar` | ? | See all-components.md for details |
| `withCodeHighlightStyles` | ? | See all-components.md for details |
| `withTypographyStyles` | ? | See all-components.md for details |


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

dmc.RichTextEditor(
    id="my-richtexteditor",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
