# TextInput

**Component**: `dmc.TextInput`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
autoComplete, debounce, description, descriptionProps, disabled, error, errorProps, inputProps, inputWrapperOrder, label, labelProps, leftSection, leftSectionPointerEvents, leftSectionProps, leftSectionWidth, n_blur, n_submit, name, persisted_props, persistence, persistence_type, placeholder, pointer, radius, readOnly, required, rightSection, rightSectionPointerEvents, rightSectionProps, rightSectionWidth, size, spellCheck, value, withAsterisk, withErrorStyles, wrapperProps
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `autoComplete` | ? | See all-components.md for details |
| `debounce` | ? | See all-components.md for details |
| `description` | ? | See all-components.md for details |
| `descriptionProps` | ? | See all-components.md for details |
| `disabled` | ? | See all-components.md for details |
| `error` | ? | See all-components.md for details |
| `errorProps` | ? | See all-components.md for details |
| `inputProps` | ? | See all-components.md for details |
| `inputWrapperOrder` | ? | See all-components.md for details |
| `label` | ? | See all-components.md for details |
| `labelProps` | ? | See all-components.md for details |
| `leftSection` | ? | See all-components.md for details |
| `leftSectionPointerEvents` | ? | See all-components.md for details |
| `leftSectionProps` | ? | See all-components.md for details |
| `leftSectionWidth` | ? | See all-components.md for details |
| `n_blur` | ? | See all-components.md for details |
| `n_submit` | ? | See all-components.md for details |
| `name` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `placeholder` | ? | See all-components.md for details |
| `pointer` | ? | See all-components.md for details |
| `radius` | ? | See all-components.md for details |
| `readOnly` | ? | See all-components.md for details |
| `required` | ? | See all-components.md for details |
| `rightSection` | ? | See all-components.md for details |
| `rightSectionPointerEvents` | ? | See all-components.md for details |
| `rightSectionProps` | ? | See all-components.md for details |
| `rightSectionWidth` | ? | See all-components.md for details |
| `size` | ? | See all-components.md for details |
| `spellCheck` | ? | See all-components.md for details |
| `value` | ? | See all-components.md for details |
| `withAsterisk` | ? | See all-components.md for details |
| `withErrorStyles` | ? | See all-components.md for details |
| `wrapperProps` | ? | See all-components.md for details |


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

dmc.TextInput(
    id="my-textinput",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
