---
layout: default
title: "Custom Joystick Suite"
parent: "Mobile Cross-Platform Input"
nav_order: 1
---

# Custom Joystick Suite

AS1 includes 4 specialized joystick implementations in `Assets/AS1/Scripts/Input/DecnetJoystick/`:

---

## Joystick Variants

1. **`FixedDecnetJoystick`**: Stays locked at a predefined anchored screen coordinate.
2. **`DynamicDecnetJoystick`**: Appears wherever the player first places their thumb within the designated touch boundary.
3. **`FloatingDecnetJoystick`**: The joystick center point drifts with the finger once dragged beyond the maximum radius.
4. **`VariableDecnetJoystick`**: Dynamic mode switching between Fixed and Floating behaviors based on user settings.
