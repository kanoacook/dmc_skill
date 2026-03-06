# DatePicker

**Component**: `dmc.DatePicker`

**Version**: 2.4.0

---

## Props

The following props are specific to this component:

```
allowDeselect, allowSingleDateInRange, ariaLabels, columnsToScroll, decadeLabelFormat, defaultDate, disabledDates, firstDayOfWeek, getDayProps, getMonthControlProps, getYearControlProps, hasNextLevel, headerControlsOrder, hideOutsideDates, hideWeekdays, level, maxDate, maxLevel, minDate, monthLabelFormat, monthsListFormat, nextIcon, nextLabel, numberOfColumns, persisted_props, persistence, persistence_type, presets, previousIcon, previousLabel, renderDay, size, type, value, weekdayFormat, weekendDays, withCellSpacing, withWeekNumbers, yearLabelFormat, yearsListFormat
```

### Detailed Props

| Prop | Type | Description |
|------|------|-------------|
| `allowDeselect` | ? | See all-components.md for details |
| `allowSingleDateInRange` | ? | See all-components.md for details |
| `ariaLabels` | ? | See all-components.md for details |
| `columnsToScroll` | ? | See all-components.md for details |
| `decadeLabelFormat` | ? | See all-components.md for details |
| `defaultDate` | ? | See all-components.md for details |
| `disabledDates` | ? | See all-components.md for details |
| `firstDayOfWeek` | ? | See all-components.md for details |
| `getDayProps` | ? | See all-components.md for details |
| `getMonthControlProps` | ? | See all-components.md for details |
| `getYearControlProps` | ? | See all-components.md for details |
| `hasNextLevel` | ? | See all-components.md for details |
| `headerControlsOrder` | ? | See all-components.md for details |
| `hideOutsideDates` | ? | See all-components.md for details |
| `hideWeekdays` | ? | See all-components.md for details |
| `level` | ? | See all-components.md for details |
| `maxDate` | ? | See all-components.md for details |
| `maxLevel` | ? | See all-components.md for details |
| `minDate` | ? | See all-components.md for details |
| `monthLabelFormat` | ? | See all-components.md for details |
| `monthsListFormat` | ? | See all-components.md for details |
| `nextIcon` | ? | See all-components.md for details |
| `nextLabel` | ? | See all-components.md for details |
| `numberOfColumns` | ? | See all-components.md for details |
| `persisted_props` | ? | See all-components.md for details |
| `persistence` | ? | See all-components.md for details |
| `persistence_type` | ? | See all-components.md for details |
| `presets` | ? | See all-components.md for details |
| `previousIcon` | ? | See all-components.md for details |
| `previousLabel` | ? | See all-components.md for details |
| `renderDay` | ? | See all-components.md for details |
| `size` | ? | See all-components.md for details |
| `type` | ? | See all-components.md for details |
| `value` | ? | See all-components.md for details |
| `weekdayFormat` | ? | See all-components.md for details |
| `weekendDays` | ? | See all-components.md for details |
| `withCellSpacing` | ? | See all-components.md for details |
| `withWeekNumbers` | ? | See all-components.md for details |
| `yearLabelFormat` | ? | See all-components.md for details |
| `yearsListFormat` | ? | See all-components.md for details |


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

dmc.DatePicker(
    id="my-datepicker",
    # Add your props here
)
```

---

## See Also

- **Full reference**: `references/all-components.md`
- **Common mistakes**: `references/common-mistakes.md`
- **Callback patterns**: `references/patterns.md`
