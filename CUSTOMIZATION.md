# 🎨 Customization Guide

## Color Theme

The profile uses a consistent **dark blue gradient** theme:
- Primary: `#2C5364`
- Secondary: `#203A43`
- Dark: `#0F2027`

To change the theme, update these values in:
1. **Header/Footer banners** — `color=` parameter in capsule-render URLs
2. **Typing SVG** — `color=` parameter
3. **Visitor counter** — `color=` parameter
4. **GitHub widgets** — `theme=` parameter (currently `tokyonight`)

## Changing the Typing Animation

Edit the `lines=` parameter in the typing SVG URL:
```
https://readme-typing-svg.demolab.com?...
&lines=First+Line;Second+Line;Third+Line
```
Use `+` for spaces and `;` to separate lines.

## Adding New Projects

Copy one of the existing project cards in the Featured Projects table and update:
- Project title and emoji
- Status badge
- Description
- Key features
- Tech stack tags
- GitHub repo link

## Adding Certifications

Add a new `<td>` cell to the certifications table with:
- An icon (use [icons8.com](https://icons8.com) or [simpleicons.org](https://simpleicons.org))
- Certification name in bold
- Issuer as subtitle

## Changing Widget Themes

All GitHub stat widgets use the `tokyonight` theme. Available themes:
- `radical`, `merko`, `gruvbox`, `dracula`, `onedark`, `cobalt`, `synthwave`, `highcontrast`, `dark`

Change the `theme=` parameter across all widget URLs for consistency.

## Skill Icons

Tech stack icons are from [skillicons.dev](https://skillicons.dev). To add/remove icons:
1. Visit [skillicons.dev](https://skillicons.dev)
2. Select your technologies
3. Copy the generated URL
4. Replace the existing `<img>` src in the Tech Stack section
