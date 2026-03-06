# Dash Mantine Components v2.4.0 Skill

**Accurate, version-pinned prop references for dash-mantine-components to prevent hallucinated attributes and runtime errors.**

## Problem

Claude frequently suggests props that don't exist in dash-mantine-components, causing `AttributeError` at runtime:
- ❌ `icon=` instead of `leftSection=` (v1 prop removed)
- ❌ `onChange=` callbacks (not supported in Dash)
- ❌ `color="primary"` (not a Mantine color)
- ❌ Props with typos or snake_case instead of camelCase

## Solution

This custom Claude skill provides **authoritative, extracted prop references** for all 181 DMC components directly from the installed v2.4.0 package.

## Installation

### For Claude Code Users

1. **Copy the skill to your local skills directory**:
   ```bash
   git clone https://github.com/kanoacook/dmc_skill.git ~/.claude/skills/dash-mantine-components
   ```

2. **Optional: Add global trigger** (`~/.claude/CLAUDE.md`):
   ```markdown
   ## Dash Mantine Components

   When code uses `dash_mantine_components`, automatically apply the dash-mantine-components skill.
   - Only use documented props from `references/all-components.md`
   - Never suggest v1 props: no `icon=`, `leftIcon=`, `rightIcon=`, `spacing=`
   - Use Dash callbacks, not JS handlers like `onChange=`, `onClick=`
   ```

3. **Use the skill**:
   ```
   /dash-mantine-components
   ```

## What's Included

### 📋 SKILL.md
- Skill overview and core rules
- Quick reference for common mistakes
- Working code examples
- How to use guide

### 📚 references/all-components.md
**181 components** with exact prop lists extracted from the installed package:
- `Button`, `TextInput`, `Select`, `Modal`, `Drawer`, `Tabs`, `Accordion`, etc.
- Every prop exactly as it appears in the package
- Shared style/layout props documented once at bottom
- No guessing, no hallucinations — only real props

### 🔧 references/common-mistakes.md
**Migration guide** for common errors:

| ❌ Wrong | ✅ Correct | Reason |
|---------|-----------|--------|
| `icon=` | `leftSection=` / `rightSection=` | v1 prop removed |
| `onChange=` | Dash callback on `value` | No JS handlers |
| `onClick=` | `n_clicks` + callback | No JS handlers |
| `leftIcon=` | `leftSection=` | v1 name |
| `spacing=` | `gap=` | v1 renamed |
| `color="primary"` | `color="blue"` | Use Mantine colors |
| `label=` (Button) | `children=` | Button has no label |
| `value=` without `id=` | Add `id="..."` | Required for callbacks |

### 🎯 references/patterns.md
**15+ working patterns** with complete code:
- Button clicks with `n_clicks` callback
- TextInput with value callback
- Select/MultiSelect dropdowns
- Modal toggle with `opened=` state
- Form validation
- Tabs, Accordions, Drawers
- Checkboxes, Switches, Radio buttons
- Chained callbacks & State patterns
- File uploads
- Theme switching

## Key Features

✅ **Version-pinned** — Extracted from DMC v2.4.0
✅ **Authoritative** — Props extracted via Python introspection
✅ **181 components** — Complete coverage
✅ **No hallucinations** — Only real, documented props
✅ **v1→v2 guide** — Common migration errors documented
✅ **Working patterns** — 15+ production-ready callback examples
✅ **Auto-trigger** — Can be configured in CLAUDE.md

## Core Rules

1. **Only use documented props** — Check `all-components.md`
2. **camelCase props** — `leftSection`, never `left_section`
3. **No v1 props** — No `icon=`, `spacing=`, `leftIcon=`
4. **No JS handlers** — Use Dash callbacks for all interactivity
5. **Components need `id=`** — Required to read/write in callbacks
6. **Always wrap in MantineProvider** — Required at app root
7. **Use real colors** — `"blue"`, `"red"`, `"green"`; not semantic tokens
8. **Follow Dash patterns** — Use correct callback syntax

## Quick Example

### ✅ Correct
```python
import dash_mantine_components as dmc
from dash import callback, Input, Output

app.layout = dmc.MantineProvider(
    children=[
        dmc.Button(
            id="submit-btn",
            children="Submit",
            color="blue",
            n_clicks=0,
        ),
        dmc.Text(id="output"),
    ]
)

@callback(
    Output("output", "children"),
    Input("submit-btn", "n_clicks"),
)
def on_click(n_clicks):
    return f"Clicked {n_clicks} times"
```

### ❌ Wrong (will cause errors)
```python
# These will all cause AttributeError or not work:
dmc.Button(icon="☑️", onChange=print)  # icon= removed, onChange not allowed
dmc.TextInput(color="primary")          # primary not a Mantine color
dmc.Select(options=[...])               # should be data=
dmc.Modal(position="center")            # Modal doesn't have position
```

## Usage Tips

1. **Look up your component** in `all-components.md`
2. **Check common mistakes** for v1→v2 migrations
3. **Reference patterns.md** for callback syntax
4. **Verify camelCase** — all props must be camelCase
5. **Always add `id=`** to interactive components

## Component Coverage

- **Form inputs**: TextInput, Textarea, NumberInput, PasswordInput, Select, MultiSelect, Autocomplete, Checkbox, Radio, Switch, etc.
- **Layouts**: Box, Container, Center, Stack, Group, Flex, Grid, SimpleGrid, etc.
- **Modals & Overlays**: Modal, Drawer, Popover, HoverCard, Tooltip, etc.
- **Navigation**: Tabs, Accordion, NavLink, Breadcrumbs, Pagination, etc.
- **Data Display**: Table, Tree, Timeline, Badge, Avatar, etc.
- **Charts**: LineChart, BarChart, AreaChart, PieChart, DonutChart, RadarChart, ScatterChart, BubbleChart, CompositeChart
- **Feedback**: Alert, Notification, Progress, Loader, Skeleton, etc.
- **Typography**: Title, Text, Code, Mark, Highlight, etc.
- **Media**: Image, BackgroundImage, Carousel, etc.
- **And 100+ more...**

## Updating for New Versions

To update when DMC releases a new version:

1. Update the installed package:
   ```bash
   pip install --upgrade dash-mantine-components
   ```

2. Re-run the introspection script (see below)

3. Update version numbers in `SKILL.md`, `references/all-components.md`, and `README.md`

### Introspection Script

```python
import dash_mantine_components as dmc
import inspect

STYLE_PROPS = {
    'm','my','mx','mt','mb','ml','mr','ms','me',
    'p','py','px','pt','pb','pl','pr','ps','pe',
    'c','bg','w','h','miw','maw','mih','mah',
    'pos','top','left','bottom','right','inset',
    'display','flex','opacity','ff','fz','fw',
    'lts','ta','lh','fs','tt','td','bd','bdrs',
    'bgsz','bgp','bgr','bga',
}

COMMON_PROPS = {
    'id','className','style','loading_state','tabIndex',
    'hiddenFrom','visibleFrom','lightHidden','darkHidden',
    'mod','classNames','styles','unstyled','variant',
    'attributes','kwargs',
}

components = [x for x in dir(dmc) if not x.startswith('_') and isinstance(getattr(dmc, x), type)]

for name in sorted(components):
    comp = getattr(dmc, name)
    try:
        sig = inspect.signature(comp.__init__)
        params = [
            p for p in sig.parameters.keys()
            if p != 'self' and p not in STYLE_PROPS and p not in COMMON_PROPS
        ]
        print(f"### {name}\n\n`{', '.join(params)}`\n")
    except Exception:
        pass
```

## Related Resources

- **Official Docs**: https://www.dash-mantine-components.com/
- **Mantine Docs**: https://mantine.dev/
- **Dash Docs**: https://dash.plotly.com/
- **Discord**: https://discord.gg/TH3QDBZXAA (Mantine)

## License

MIT

## Contributing

Found a mistake in the references or want to add more patterns? Open an issue or PR!

## Changelog

### v2.4.0 (2026-03-06)
- Initial release
- 181 components covered
- 15+ working patterns
- v1→v2 migration guide
- Auto-trigger via CLAUDE.md

---

**Questions?** Open an issue on GitHub or check the skill files directly.
