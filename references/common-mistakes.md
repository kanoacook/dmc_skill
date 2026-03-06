# Common DMC Mistakes — Props That Don't Exist

This guide documents the most frequent prop errors when using dash-mantine-components. All of these will cause **runtime AttributeError**.

---

## Version Migration Errors (v1 → v2)

| ❌ WRONG | ✅ CORRECT | Component(s) | Note |
|---------|-----------|--------------|------|
| `icon=` | `leftSection=` or `rightSection=` | Button, Badge, ActionIcon, NavLink, TextInput, etc. | v1 prop removed; use leftSection/rightSection with icon components |
| `leftIcon=` | `leftSection=` | Button, ActionIcon, TextInput, Select, etc. | v1 name; v2 uses leftSection |
| `rightIcon=` | `rightSection=` | Button, ActionIcon, TextInput, Select, etc. | v1 name; v2 uses rightSection |
| `spacing=` | `gap=` | Stack, Group, Flex | v1 prop renamed in v2 |
| `label=` (on Button) | `children=` | Button | Button has no label prop; use children instead |
| `withBorder=` (on Badge) | `variant="outline"` | Badge | Badge has no withBorder; use variant instead |
| `defaultValue=` | `value=` + `defaultValue=` logic in callback | Most inputs | Dash uses value + callback, not just defaultValue |
| `disabled=` (on Group) | _No direct prop_ | Group | Group doesn't disable children; wrap children in disabled wrapper |

---

## Common Typos & Misspellings

| ❌ WRONG | ✅ CORRECT | Component(s) |
|---------|-----------|--------------|
| `lavelProps=` | `labelProps=` | Input components |
| `descritionProps=` | `descriptionProps=` | Input components |
| `visibile=` | `visible=` | PasswordInput |
| `onFocus=` | _Use Dash callback_ | All inputs |
| `onChange=` | _Use Dash callback on value_ | All inputs |
| `onClick=` | _Use n_clicks + callback_ | Button, ActionIcon, MenuItem |

---

## Modal & Drawer Props

| ❌ WRONG | ✅ CORRECT | Note |
|---------|-----------|------|
| `position=` | _Not a Modal prop_ | Modal doesn't accept position (use Drawer if you need positioning) |
| `onClose=` | _Use Dash callback_ | Handle opened=False in callback |
| `actions=` | _Not standard_ | Use custom layout inside children |
| `backdrop=` | `withOverlay=True` | Backdrop shown via withOverlay |

---

## Color & Styling Props

| ❌ WRONG | ✅ CORRECT | Note |
|---------|-----------|------|
| `color="primary"` | `color="blue"` (or another Mantine color) | Use actual Mantine colors: blue, red, green, gray, etc. Not semantic tokens |
| `color="secondary"` | `color="teal"` or another color | Mantine uses specific color names, not semantic names |
| `style={"color": "red"}` | Use `c="red"` prop instead | Prefer shorthand props; style dict works but less clean |

---

## Input/Select Specific

| ❌ WRONG | ✅ CORRECT | Component(s) | Note |
|---------|-----------|--------------|------|
| `options=` | `data=` | Select, MultiSelect, Autocomplete | Dash Mantine uses `data=` for dropdown options |
| `placeholder=` (no children) | `children=[dmc.Option(...)]` | Select (when using raw Option children) | Select requires structured Option children or data= list |
| `value=` without `id=` | Add `id="..."` | All input components | Can't use value in callbacks without id |
| `clearable=True` without `clearButtonProps=` | Add `clearButtonProps={}` if custom clear styling needed | Text/Number/Select inputs | clearable=True enables default clear; customize with clearButtonProps |

---

## Date & Time Components

| ❌ WRONG | ✅ CORRECT | Component(s) |
|---------|-----------|--------------|
| `value=None` | Use `allowDeselect=True` | DatePicker, DateInput | Set allowDeselect=True for nullable dates |
| `format="DD/MM/YYYY"` | `valueFormat="DD/MM/YYYY"` | DateInput, DatePickerInput | Use valueFormat for display format |
| `startDate=` / `endDate=` | `type="range"` + `value=[start, end]` | DatePickerInput | Range mode uses type="range" |

---

## Callback Mistakes

| ❌ WRONG | ✅ CORRECT |
|---------|-----------|
| `n_clicks=n_clicks` in layout | `n_clicks=0` in component, then `@callback(..., Input("btn-id", "n_clicks"))` | Clicks are read via callback, not set in layout |
| `value=selected_value` in layout | `value=selected_value` in component, then `@callback(..., Output("input-id", "value"))` | Value can be initialized, then updated via Output in callback |
| `opened=opened_state` without callback | `opened=opened_state` + `@callback(Output(..., "opened"))` returning bool | Modal/Drawer need callback to toggle opened state |

---

## Style Props That Don't Exist

| ❌ WRONG | ✅ CORRECT | Category |
|---------|-----------|----------|
| `margin=` | `m=`, `my=`, `mx=`, `mt=`, `mb=`, `ml=`, `mr=` | Spacing |
| `padding=` | `p=`, `py=`, `px=`, `pt=`, `pb=`, `pl=`, `pr=` | Spacing |
| `textAlign=` | `ta=` | Typography |
| `fontSize=` | `fz=` | Typography |
| `fontWeight=` | `fw=` | Typography |
| `backgroundColor=` | `bg=` | Color |
| `textColor=` | `c=` | Color |
| `width=` | `w=` | Sizing |
| `height=` | `h=` | Sizing |
| `border=` (style string) | Use `bd="1px solid black"` or `style={"border": "1px solid black"}` | Borders |

---

## Provider & Layout Mistakes

| ❌ WRONG | ✅ CORRECT | Note |
|---------|-----------|------|
| App without `MantineProvider` | Wrap root in `dmc.MantineProvider(children=[...])` | All DMC apps need MantineProvider at root |
| `theme={}` passed to component | `theme={}` passed to MantineProvider | Theme config goes on MantineProvider, not individual components |
| Multiple MantineProviders | Single MantineProvider at app root only | Only one MantineProvider per app |

---

## Summary: Most Common Mistakes

1. **`icon=` instead of `leftSection=`** — biggest source of errors
2. **`onChange=` instead of Dash callback** — Event handlers don't work in Dash
3. **`value=` without `id=`** — Can't read/write values in callbacks without id
4. **Wrong color names** — use `"blue"`, `"red"`, `"green"`, etc.; not `"primary"`, `"secondary"`
5. **`spacing=` instead of `gap=`** — v1 prop rename
6. **Missing MantineProvider** — required at root of app
7. **Forgetting to add `children=`** — Most components default to children positional arg, but explicit `children=` is clearer

---

## How to Debug

If you get `AttributeError: 'Button' object has no attribute 'xyz'`:

1. **Check all-components.md** — Look up your component and verify prop exists
2. **Check this file** — Common migration mistakes?
3. **Verify camelCase** — Is it `leftSection=` not `left_section=`?
4. **Check Dash callbacks** — Are you trying to use JS handlers like `onChange=` or `onClick=`?
5. **Search docs** — https://www.dash-mantine-components.com/

---

## Quick Checklist

- [ ] Using `leftSection=`/`rightSection=` instead of `icon=`?
- [ ] Using Dash callbacks instead of `onChange=`/`onClick=`?
- [ ] All components using camelCase props?
- [ ] Callback-read components have `id=`?
- [ ] Root wrapped in `dmc.MantineProvider`?
- [ ] Using real Mantine colors (blue, red, green) not semantic tokens?
