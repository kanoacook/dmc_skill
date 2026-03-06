# StepperStep

**Component**: `dmc.StepperStep`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
allowStepClick, allowStepSelect, children, color, completedIcon, description, icon, iconPosition, iconSize, label, loading, orientation, progressIcon, state, step, withIcon
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `allowStepClick` | ? | See all-components.md for details |
| `allowStepSelect` | ? | See all-components.md for details |
| `children` | ? | See all-components.md for details |
| `color` | ? | See all-components.md for details |
| `completedIcon` | ? | See all-components.md for details |
| `description` | ? | See all-components.md for details |
| `icon` | ? | See all-components.md for details |
| `iconPosition` | ? | See all-components.md for details |
| `iconSize` | ? | See all-components.md for details |
| `label` | ? | See all-components.md for details |
| `loading` | ? | See all-components.md for details |
| `orientation` | ? | See all-components.md for details |
| `progressIcon` | ? | See all-components.md for details |
| `state` | ? | See all-components.md for details |
| `step` | ? | See all-components.md for details |
| `withIcon` | ? | See all-components.md for details |


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

dmc.StepperStep(
    id="my-stepperstep",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
