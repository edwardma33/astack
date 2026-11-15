---
name: change-theme
description: Change an app's overall visual theme using a named TweakCN theme or a user's description, and apply it consistently across the project.
---

# Change the app's theme

Help the user change how the whole app looks. Speak in terms of colors, fonts, corners, and the app's appearance. Do not require the user to understand CSS, shadcn/ui, or design tokens.

## Choose the theme

- If the user names a TweakCN theme or provides its link, use that theme. Resolve the exact theme from [TweakCN](https://tweakcn.com/) or its registry before applying it. Do not ask for confirmation when the intended theme is clear.
- If the user describes a look, such as warm brown, inspect the available TweakCN themes and choose a suitable starting point. When there are meaningful alternatives, briefly describe a few and offer a recommendation. Ask for a choice when the preference matters; otherwise make a reasonable choice and tell the user what you picked. If a close theme needs small changes to match the request, adjust it.
- If the theme cannot be found or TweakCN is unavailable, say what you could not verify. Ask for a theme link or exported CSS, or offer to adapt the existing theme to the requested look. Do not invent a theme name or silently claim that a custom theme came from TweakCN.

## Apply it across the project

Inspect the app's existing styling setup first. Find the global stylesheet, shadcn configuration, Tailwind version, theme provider or light/dark mode, and shared components. Preserve the current layout, functionality, unrelated custom CSS, and intentional semantic colors such as error and success states unless the user asks to change them.

Use the selected theme's official registry item or exported CSS, choosing the format compatible with the project. When using the shadcn CLI to install a registry item, inspect its effects first and merge its theme changes without overwriting unrelated work. Update the app's existing global theme variables and their Tailwind mappings for the supported light and dark modes. Preserve variables the app needs that the theme does not define. Include the theme's font, radius, and shadow settings when provided and applicable; do not introduce a runtime theme picker unless requested.

Check shared layouts, pages, and components for hard-coded visual colors or local overrides that prevent the requested theme from appearing consistently. Replace the relevant presentation values with the project's semantic theme tokens, or add shared tokens where needed. Keep content-specific colors, images, and brand assets that are intentionally fixed. Ensure readable foreground/background contrast and visible focus states in each supported mode. Avoid changing the shadcn component style or rebuilding components merely to change colors.

## Verify and explain

Run the project's relevant checks. When an app can run locally, inspect representative pages and shared components in the supported light and dark modes, including controls and text, and fix theme inconsistencies. If a page or state cannot be inspected, say so rather than claiming full coverage.

Tell the user which theme or custom direction was applied and how the app changed. Mention any intentional exceptions, limits, and checks performed. If helpful, explain that shared theme settings control the look across the app, so future changes can be made in one place.
