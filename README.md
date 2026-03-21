# Agent Skills

AI coding assistant context. Skill packages for implementation details, API references, and best practices.

## Skills

### PagerKit
Context for `PagerKit`, a SwiftUI library for page-based navigation.
*   **Configuration:** `PKPagesView` and `PKPage` setup.
*   **Content:** Dynamic generation (`ForEach`).
*   **Customization:** Indicators, styling, orientation.
*   **Events:** State changes, navigation direction.

### SearchBar
Context for `SearchBar`, a unified search component for SwiftUI.
*   **Styling:** Platform-adaptive styles (Capsule, Rounded, Glass).
*   **Features:** Search tokens, suggestions.
*   **Behavior:** Focus management, display modes.

### SymbolPicker
Context for `SymbolPicker`, a native SF Symbol picker for SwiftUI.
*   **Appearance:** Symbol rendering (Filled/Outlined).
*   **Color:** `SymbolColor`, SwiftUI `Color`, RGBA bindings.
*   **Interaction:** Custom dismissal behavior.

### ColorKit
Context for `ColorKit`, a library for advanced color manipulation.
*   **Color Spaces:** RGB, HSL, CMYK, LAB, LCH, OKLAB.
*   **Conversion:** High-precision conversions.
*   **Utilities:** Hex strings, blending, luminance.
*   **Compatibility:** SwiftUI, UIKit, AppKit.

## Installation

### CLI
Install specific skills:

```bash
npx skills add https://github.com/szpakkamil/agentskills --skill PagerKit
npx skills add https://github.com/szpakkamil/agentskills --skill SearchBar
npx skills add https://github.com/szpakkamil/agentskills --skill SymbolPicker
npx skills add https://github.com/szpakkamil/agentskills --skill ColorKit
```

### Team Configuration
Enable automatically in `.claude/settings.json`:

```json
{
  "enabledPlugins": {
    "PagerKit@agent-skills": true,
    "SearchBar@agent-skills": true,
    "SymbolPicker@agent-skills": true,
    "ColorKit@agent-skills": true
  },
  "extraKnownMarketplaces": {
    "agent-skills": {
      "source": { "source": "github", "repo": "szpakkamil/agentskills" }
    }
  }
}
```

### Manual
Clone the repository. Direct your AI assistant to the specific skill directory (`/PagerKit`, `/SymbolPicker`, `/SearchBar`, `/ColorKit`).

## Structure

Adheres to the [Agent Skills](https://agentskills.io/home) open format.
*   **SKILL.md:** Decision logic and usage patterns.
*   **references/:** API documentation and examples.

## License

Copyright © 2026 Kamil Szpak.
MIT License. See [LICENSE.md](LICENSE.md).
