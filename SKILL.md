---
name: dash-mantine-components
description: Accurate prop references for dash-mantine-components v2.4.0. Use when writing, reviewing, or fixing DMC component code to prevent hallucinated attributes and ensure valid Dash callbacks.
license: MIT
metadata:
  version: "2.4.0"
  components: 181
  generated: "2026-03-06"
---

# Dash Mantine Components v2.4.0 Skill

This skill provides authoritative, version-pinned prop references for **dash-mantine-components** (DMC) extracted directly from the installed package. Use this skill to write correct DMC code and avoid common runtime errors.

---

## When to Use This Skill

- ✅ Writing new DMC components
- ✅ Debugging `AttributeError: 'Component' object has no attribute 'xyz'`
- ✅ Reviewing DMC code for prop validity
- ✅ Migrating from v1 → v2
- ✅ Building Dash forms, modals, tables, charts
- ✅ Implementing Dash callbacks for DMC components

---

## Core Rules

1. **Only use documented props** — Check `references/all-components.md` for exact prop lists
2. **camelCase props** — `leftSection`, `rightSection`, `fullWidth`, never snake_case
3. **No JS event handlers** — No `onChange=`, `onClick=`, `onFocus=`; use Dash callbacks only
4. **Callbacks need `id=`** — Any component read/written in a callback must have an `id`
5. **Children first** — Positional first arg `dmc.Button("Text")` or kwarg `dmc.Button(children="Text")`
6. **Wrap in MantineProvider** — All DMC apps must have root `dmc.MantineProvider(...)`

---

## Reference Files

- **`references/all-components.md`** — Authoritative prop lists for all 181 components
- **`references/common-mistakes.md`** — Common errors and their corrections (icon→leftSection, onChange→callback, etc.)
- **`references/patterns.md`** — Correct Dash callback patterns for forms, modals, selects, tabs, etc.

---

## Quick Examples

### ✅ Correct Button with Click Callback

```python
import dash_mantine_components as dmc
from dash import callback, Input, Output

dmc.Button(
    id="submit-btn",
    children="Submit",
    color="blue",
    n_clicks=0,  # Initialize
)

@callback(
    Output("output", "children"),
    Input("submit-btn", "n_clicks"),
)
def on_click(n_clicks):
    return f"Clicked {n_clicks} times"
```

### ✅ Correct TextInput with Callback

```python
dmc.TextInput(
    id="email-input",
    label="Email",
    placeholder="your@email.com",
    required=True,
    leftSection="@",  # v2: was icon= in v1
)

@callback(
    Output("email-display", "children"),
    Input("email-input", "value"),
)
def show_email(value):
    return f"You entered: {value}"
```

### ✅ Correct Modal Toggle

```python
dmc.Modal(
    id="my-modal",
    opened=False,
    title="Modal Title",
    children=[dmc.Text("Content here")],
)

@callback(
    Output("my-modal", "opened"),
    Input("open-btn", "n_clicks"),
    prevent_initial_call=True,
)
def toggle_modal(n_clicks):
    return n_clicks > 0
```

### ✅ Correct Select Dropdown

```python
dmc.Select(
    id="color-select",
    label="Pick a color",
    data=[
        {"value": "blue", "label": "Blue"},
        {"value": "red", "label": "Red"},
    ],
    value="blue",
)

@callback(
    Output("color-display", "children"),
    Input("color-select", "value"),
)
def show_color(value):
    return f"Selected: {value}"
```

---

## Common Mistakes & Fixes

### ❌ `icon=` → ✅ `leftSection=` / `rightSection=`
- **Problem**: v1 prop `icon=` was removed
- **Solution**: Use `leftSection=` or `rightSection=` with icon component
- **Example**: `dmc.Button(leftSection=dmc.ThemeIcon(...), children="Click me")`

### ❌ `onChange=` → ✅ Dash Callback
- **Problem**: DMC doesn't have JS event handlers
- **Solution**: Use Dash `@callback` with `Input("id", "value")`
- **Example**: See "Correct TextInput" above

### ❌ `value=` without `id=` → ✅ Add `id=`
- **Problem**: Can't read/write values in callbacks without id
- **Solution**: Always add `id="something"` to interactive components

### ❌ `spacing=` → ✅ `gap=`
- **Problem**: v1 prop renamed
- **Solution**: Use `gap=` in Stack, Group, Flex

### ❌ `color="primary"` → ✅ `color="blue"`
- **Problem**: Mantine uses color names, not semantic tokens
- **Solution**: Use actual color names: `"blue"`, `"red"`, `"green"`, `"gray"`, etc.

---

## Shared Props (All Components)

These work on **every DMC component** — you don't need to check per-component:

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

## How to Use This Skill

### Step 1: Identify Your Component
Find your component name in `references/all-components.md` (e.g., "Button", "Select", "Modal")

### Step 2: Check Allowed Props
Read the prop list for your component. All props must be from that list or shared props above.

### Step 3: Verify Common Mistakes
Check `references/common-mistakes.md` — is your prop a known mistake? (e.g., `icon=` should be `leftSection=`)

### Step 4: Reference Patterns
See `references/patterns.md` for correct callback syntax for your use case (buttons, selects, forms, etc.)

### Step 5: Implement with Confidence
Use only props from the authoritative lists. You're now guaranteed to generate valid DMC code.

---

## Troubleshooting

### I get `AttributeError: 'Button' object has no attribute 'xyz'`

1. Check `references/all-components.md` for Button
2. Verify your prop name matches exactly (camelCase)
3. Check `references/common-mistakes.md` — is it a known v1→v2 migration?
4. Search for similar props in the component's list

### My callback doesn't trigger

1. Verify component has `id="something"`
2. Verify callback `Input()` references the correct id and property
3. For value changes: use `Input("id", "value")`
4. For button clicks: use `Input("id", "n_clicks")`
5. For modal/drawer: use `Output("id", "opened")` returning boolean

### My component doesn't style correctly

1. Use shorthand spacing props: `m=10`, `p="md"`, `c="red"`, `bg="blue"`
2. Or use `style={}` dict with CSS properties
3. Never use `margin=`, `padding=`, `color=`, `backgroundColor=` (not valid DMC props)
4. For custom styling, use `className=` and define in CSS

---

## Version Info

- **DMC Version**: 2.4.0
- **Total Components**: 181
- **Props Extracted From**: `/Users/kanoa/.pyenv/versions/3.12.12/lib/python3.12/site-packages/dash_mantine_components`
- **Generated**: 2026-03-06
- **Last Updated**: 2026-03-06

---

## Key Reminders

| Do | Don't |
|---|---|
| Use `leftSection=`, `rightSection=` | Use `icon=`, `leftIcon=`, `rightIcon=` |
| Use Dash callbacks for interactivity | Use `onChange=`, `onClick=`, `onFocus=` |
| Use `gap=` in layouts | Use `spacing=` |
| Use real colors: "blue", "red", "green" | Use semantic: "primary", "secondary" |
| Use `data=` for select options | Use `options=` |
| Start with `dmc.MantineProvider` | Forget to wrap your app |
| Add `id=` to interactive components | Read/write values without `id=` |
| Use camelCase for props | Use snake_case for props |

---

## Still Stuck?

- **Check patterns.md** — See full working examples for your use case
- **Check all-components.md** — Verify prop exists and spelling is exact
- **Check common-mistakes.md** — Is it a known migration issue?
- **Ask Claude directly** — "I'm getting AttributeError with Button prop 'xyz'"

---

## License

MIT
