# Dash Mantine Components — Correct Patterns

Essential patterns for working with dash-mantine-components v2.4.0. All examples use Python Dash with the `@callback` decorator.

---

## 1. Basic App Setup

```python
import dash_mantine_components as dmc
from dash import Dash, callback, Input, Output

app = Dash(__name__)

app.layout = dmc.MantineProvider(
    children=[
        dmc.Container(
            children=[
                dmc.Title("My App", order=1),
                # Components here
            ],
            my=20,
        )
    ]
)

if __name__ == "__main__":
    app.run_server(debug=True)
```

**Key Points**:
- Wrap entire app in `dmc.MantineProvider(...)`
- Use `dmc.Container` for layout
- All interactive components need `id=` to be used in callbacks

---

## 2. Text Input with Value Callback

```python
import dash_mantine_components as dmc
from dash import callback, Input, Output

app.layout = dmc.MantineProvider(
    children=[
        dmc.TextInput(
            id="username-input",
            label="Username",
            placeholder="Enter your username",
            required=True,
        ),
        dmc.Text(id="username-output", mt=10),
    ]
)

@callback(
    Output("username-output", "children"),
    Input("username-input", "value"),
)
def update_output(username):
    if not username:
        return "Enter a username above"
    return f"Hello, {username}!"
```

**Key Points**:
- Input component has `id=`
- Read value via `Input("id", "value")`
- Update text via `Output("id", "children")` for Text component

---

## 3. Button with Click Counting

```python
dmc.Button(
    id="submit-button",
    children="Submit",
    color="blue",
    n_clicks=0,  # Initialize to 0
),
dmc.Text(id="click-count", mt=10),

@callback(
    Output("click-count", "children"),
    Input("submit-button", "n_clicks"),
)
def count_clicks(n_clicks):
    return f"Button clicked {n_clicks} times"
```

**Key Points**:
- Button tracking uses `n_clicks` property (not `onClick=`)
- Initialize `n_clicks=0`
- Read via `Input("id", "n_clicks")`

---

## 4. Modal Toggle

```python
dmc.Button(
    id="open-modal-btn",
    children="Open Modal",
    n_clicks=0,
),
dmc.Modal(
    id="my-modal",
    opened=False,  # Start closed
    title="Modal Title",
    children=[
        dmc.Text("This is modal content"),
    ],
),

@callback(
    Output("my-modal", "opened"),
    Input("open-modal-btn", "n_clicks"),
    prevent_initial_call=True,  # Don't trigger on page load
)
def toggle_modal(n_clicks):
    return True  # Return boolean for opened state
```

**Key Points**:
- Modal `opened=` prop toggles visibility
- Output to `"opened"` property
- Return boolean (True/False)
- Use `prevent_initial_call=True` to avoid flashing on load

---

## 5. Select / Dropdown

```python
dmc.Select(
    id="color-select",
    label="Choose a color",
    data=[
        {"value": "blue", "label": "Blue"},
        {"value": "red", "label": "Red"},
        {"value": "green", "label": "Green"},
    ],
    value="blue",  # Default selection
),
dmc.Text(id="selected-color", mt=10),

@callback(
    Output("selected-color", "children"),
    Input("color-select", "value"),
)
def show_color(selected):
    return f"You selected: {selected}"
```

**Key Points**:
- Use `data=` for options (not `options=`)
- Each option is dict with `value` and `label`
- Read via `Input("id", "value")`

---

## 6. MultiSelect (Multiple Values)

```python
dmc.MultiSelect(
    id="multi-select",
    label="Choose fruits",
    data=[
        {"value": "apple", "label": "Apple"},
        {"value": "banana", "label": "Banana"},
        {"value": "orange", "label": "Orange"},
    ],
    value=["apple"],  # Start with apple selected
),
dmc.Text(id="selected-fruits", mt=10),

@callback(
    Output("selected-fruits", "children"),
    Input("multi-select", "value"),
)
def show_fruits(fruits):
    if not fruits:
        return "No fruits selected"
    return f"Selected: {', '.join(fruits)}"
```

**Key Points**:
- `value=` is a list of selected values
- Returns list in callback
- Check `if not fruits` to detect empty selection

---

## 7. Form with Validation

```python
dmc.TextInput(
    id="email-input",
    label="Email",
    placeholder="your@email.com",
    error="Invalid email",  # Shows error message
),
dmc.NumberInput(
    id="age-input",
    label="Age",
    value=18,
    min=0,
    max=120,
),
dmc.Button(
    id="form-submit",
    children="Submit",
    n_clicks=0,
),
dmc.Text(id="form-result", mt=10),

@callback(
    Output("form-result", "children"),
    Input("form-submit", "n_clicks"),
    Input("email-input", "value"),
    Input("age-input", "value"),
    prevent_initial_call=True,
)
def submit_form(n_clicks, email, age):
    if not email or "@" not in email:
        return "Invalid email"
    if not age or age < 18:
        return "Must be 18 or older"
    return f"Welcome, {email}! (age {age})"
```

**Key Points**:
- Multiple inputs in single callback
- Validate before processing
- Return error message if invalid
- Use `prevent_initial_call=True`

---

## 8. Checkbox & Switch

```python
dmc.Checkbox(
    id="agree-checkbox",
    label="I agree to terms",
    checked=False,  # Start unchecked
),
dmc.Switch(
    id="dark-mode-switch",
    label="Dark Mode",
    checked=False,
),
dmc.Text(id="checkbox-output", mt=10),

@callback(
    Output("checkbox-output", "children"),
    Input("agree-checkbox", "checked"),
    Input("dark-mode-switch", "checked"),
)
def show_selections(agreed, dark_mode):
    msg = "Agreement: " + ("✓" if agreed else "✗")
    msg += " | Dark mode: " + ("ON" if dark_mode else "OFF")
    return msg
```

**Key Points**:
- Use `checked=` prop (not `value=`)
- Read via `Input("id", "checked")`
- Returns boolean

---

## 9. Tabs

```python
dmc.Tabs(
    id="tabs",
    value="tab1",  # Active tab
    children=[
        dmc.TabsList(
            children=[
                dmc.TabsTab("Home", value="tab1"),
                dmc.TabsTab("Profile", value="tab2"),
                dmc.TabsTab("Settings", value="tab3"),
            ]
        ),
        dmc.TabsPanel(
            value="tab1",
            children=[dmc.Text("Home content")],
        ),
        dmc.TabsPanel(
            value="tab2",
            children=[dmc.Text("Profile content")],
        ),
        dmc.TabsPanel(
            value="tab3",
            children=[dmc.Text("Settings content")],
        ),
    ],
),
dmc.Text(id="active-tab-output", mt=10),

@callback(
    Output("active-tab-output", "children"),
    Input("tabs", "value"),
)
def show_active_tab(active_tab):
    return f"Active tab: {active_tab}"
```

**Key Points**:
- TabsTab `value=` matches TabsPanel `value=`
- Tabs component has `value=` prop for active tab
- Read active tab via `Input("id", "value")`

---

## 10. Accordion

```python
dmc.Accordion(
    id="accordion",
    value=None,  # No section open by default
    children=[
        dmc.AccordionItem(
            value="section1",
            children=[
                dmc.AccordionControl("Section 1"),
                dmc.AccordionPanel(
                    dmc.Text("Content for section 1")
                ),
            ],
        ),
        dmc.AccordionItem(
            value="section2",
            children=[
                dmc.AccordionControl("Section 2"),
                dmc.AccordionPanel(
                    dmc.Text("Content for section 2")
                ),
            ],
        ),
    ],
),
dmc.Text(id="accordion-output", mt=10),

@callback(
    Output("accordion-output", "children"),
    Input("accordion", "value"),
)
def show_open_section(value):
    return f"Open section: {value}" if value else "No section open"
```

**Key Points**:
- Accordion `value=` prop tracks which section is open
- AccordionItem `value=` identifies each section
- Read via `Input("id", "value")`

---

## 11. Simple Grid Layout

```python
dmc.SimpleGrid(
    cols=3,  # 3 columns
    spacing="lg",
    children=[
        dmc.Card(
            withBorder=True,
            children=[
                dmc.Text("Card 1"),
            ],
        ),
        dmc.Card(
            withBorder=True,
            children=[
                dmc.Text("Card 2"),
            ],
        ),
        dmc.Card(
            withBorder=True,
            children=[
                dmc.Text("Card 3"),
            ],
        ),
    ],
)
```

**Key Points**:
- `cols=` sets number of columns
- `spacing=` sets gap between items
- Use `withBorder=True` for card borders

---

## 12. Popover (Tooltip)

```python
dmc.Popover(
    position="bottom",
    children=[
        dmc.PopoverTarget(
            dmc.Button("Hover me", id="popover-target"),
        ),
        dmc.PopoverDropdown(
            dmc.Text("This is popover content"),
        ),
    ],
)
```

**Key Points**:
- PopoverTarget wraps trigger element
- PopoverDropdown contains content
- `position=` sets where dropdown appears

---

## 13. Drawer (Side Panel)

```python
dmc.Button(
    id="open-drawer",
    children="Open Drawer",
    n_clicks=0,
),
dmc.Drawer(
    id="my-drawer",
    opened=False,
    title="Drawer Title",
    padding="md",
    children=[
        dmc.Text("Drawer content here"),
    ],
),

@callback(
    Output("my-drawer", "opened"),
    Input("open-drawer", "n_clicks"),
    prevent_initial_call=True,
)
def toggle_drawer(n_clicks):
    return True if n_clicks > 0 else False
```

**Key Points**:
- Drawer `opened=` prop toggles visibility
- Similar to Modal but slides from side

---

## 14. File Upload (If using dash.dcc.Upload)

```python
from dash import dcc
import base64

dcc.Upload(
    id="upload-data",
    children=[
        dmc.Button("Upload CSV"),
    ],
    multiple=False,
),
dmc.Text(id="upload-output", mt=10),

@callback(
    Output("upload-output", "children"),
    Input("upload-data", "contents"),
)
def process_upload(contents):
    if not contents:
        return "No file uploaded"
    # Decode and process
    content_type, content_string = contents.split(",")
    decoded = base64.b64decode(content_string)
    return f"Uploaded {len(decoded)} bytes"
```

**Key Points**:
- File data comes as base64 string
- Decode with `base64.b64decode()`
- This is `dash.dcc.Upload`, not DMC-specific

---

## 15. Theme Switching

```python
dmc.Select(
    id="theme-select",
    data=[
        {"value": "light", "label": "Light"},
        {"value": "dark", "label": "Dark"},
    ],
    value="light",
),

# In MantineProvider:
dmc.MantineProvider(
    theme={
        "colorScheme": "light",  # or "dark"
    },
    children=[...],
)

# Or use colorSchemeManager for persistent selection
from dash_mantine_components import MantineProvider
from dash_mantine_components.styles import theme

app.layout = dmc.MantineProvider(
    forceColorScheme="light",  # Force color scheme
    theme={"primaryColor": "blue"},
    children=[...],
)
```

**Key Points**:
- `colorScheme=` in theme dict: "light" or "dark"
- `forceColorScheme=` overrides user preference
- Use `theme={}` to customize colors

---

## Common Callback Patterns

### Pattern: State vs Input
```python
# Use Input when callback should trigger on change
@callback(
    Output("output", "children"),
    Input("button", "n_clicks"),  # Triggers callback on every click
)
def on_click(n_clicks):
    return n_clicks

# Use State when you need value but don't want to trigger on change
from dash import State

@callback(
    Output("output", "children"),
    Input("button", "n_clicks"),
    State("input", "value"),  # Read but don't trigger
    prevent_initial_call=True,
)
def on_click_with_state(n_clicks, input_value):
    return f"Clicked {n_clicks} times with value: {input_value}"
```

### Pattern: Multiple Outputs
```python
@callback(
    Output("output1", "children"),
    Output("output2", "children"),
    Input("button", "n_clicks"),
)
def update_multiple(n_clicks):
    return f"Clicks: {n_clicks}", f"You clicked {n_clicks} times"
```

### Pattern: Chained Callbacks
```python
@callback(
    Output("intermediate-store", "data"),
    Input("input", "value"),
)
def process_data(value):
    return value.upper()  # Store processed data

@callback(
    Output("output", "children"),
    Input("intermediate-store", "data"),
)
def show_result(processed):
    return f"Result: {processed}"
```

---

## Essential Rules

1. **Every interactive component needs `id=`** — Required for callbacks
2. **No JS event handlers** — No `onChange=`, `onClick=`, `onFocus=`; use callbacks
3. **Children as positional first arg or `children=` kwarg** — `dmc.Button("Text")` or `dmc.Button(children="Text")`
4. **Wrap app in MantineProvider** — Required for styling to work
5. **Use prop names exactly as listed** — `leftSection=`, not `leftSectionX=` or `left_section=`
6. **camelCase for all props** — Never snake_case
7. **Read values in callbacks via specific props** — `value=`, `checked=`, `n_clicks=`, etc.

---

## Debug Checklist

- [ ] Component has `id=`?
- [ ] Callback uses correct property (`value`, `checked`, `n_clicks`, etc.)?
- [ ] App wrapped in `dmc.MantineProvider`?
- [ ] No JS event handlers (`onChange=`, `onClick=`)?
- [ ] Props in camelCase?
- [ ] Data structures correct (list for MultiSelect, dict for Select data)?
- [ ] Callback decorated with `@callback`?
