# Agent Skills

This repository serves as a source of context for AI coding assistants. It contains specialized skill packages that provide implementation details, API references, and best practices for my Packages.

## Skills

### PagerKit
Documentation and logic for `PagerKit`, a SwiftUI library for page-based navigation.
*   **Configuration:** Setup for `PKPagesView` and `PKPage`.
*   **Content:** Dynamic generation using `ForEach`.
*   **Customization:** Indicators, styling, and orientation.
*   **Events:** Handling state changes and navigation direction.

### SearchBar
Documentation and logic for `SearchBar`, a unified search component for SwiftUI.
*   **Styling:** Platform-adaptive styles (Capsule, Rounded, Glass).
*   **Features:** Search tokens and suggestions (iOS 16+).
*   **Behavior:** Focus management and display modes.

### SymbolPicker
Documentation and logic for `SymbolPicker`, a native SF Symbol picker for SwiftUI.
*   **Appearance:** Customize symbol rendering (Filled/Outlined).
*   **Color:** Support for `SymbolColor`, SwiftUI `Color`, and RGBA bindings.
*   **Interaction:** Custom dismissal behavior.

### ColorKit
Documentation and logic for `ColorKit`, a standalone library for advanced color manipulation and conversion.
*   **Color Spaces:** Support for RGB, HSL, CMYK, LAB, LCH, and OKLAB.
*   **Conversion:** High-precision color space conversions.
*   **Utilities:** Hex string support, blending, and luminance calculations.
*   **Compatibility:** Seamless integration with SwiftUI, UIKit, and AppKit.

## Installation

### CLI (skills.sh)
To install specific skills into your environment:

```bash
npx skills add https://github.com/szpakkamil/agentskills --skill PagerKit
npx skills add https://github.com/szpakkamil/agentskills --skill SearchBar
npx skills add https://github.com/szpakkamil/agentskills --skill SymbolPicker
npx skills add https://github.com/szpakkamil/agentskills --skill ColorKit
```

### Team Configuration
To automatically enable these skills for a repository using Claude Code, configure `.claude/settings.json`:

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
Clone the repository and direct your AI assistant to the specific skill directory (`/PagerKit`, `/SymbolPicker`, `/SearchBar` or `/ColorKit`) according to its documentation.

## Structure

This repository adheres to the [Agent Skills](https://agentskills.io/home) open format.
*   **SKILL.md:** Defines the decision logic and usage patterns.
*   **references/:** Contains specific API documentation and examples.

## License

Copyright © 2026 Kamil Szpak.
MIT License. See [LICENSE.md](LICENSE.md) for details.
