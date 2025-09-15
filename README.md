# TailWind Theme for Obsidian

A modern Obsidian theme inspired by the Tailwind CSS design system, featuring enhanced typography, consistent spacing, and comprehensive color customization.

## Key Features

### Design System
- **Semantic Token Architecture**: Easy customization through two-layer variable system
- **Complete Tailwind Color System**: All official Tailwind CSS colors included
- **Responsive Design**: Mobile-first approach with desktop enhancements
- **Consistent Spacing Scale**: Based on 0.25rem (4px) units, following Tailwind's spacing conventions
- **Border Radius**: From none to full, matching Tailwind's radius scale
- **Shadows**: Multiple shadow levels for depth and hierarchy

### Theme Support
- **Dark Theme**: Primary theme with dark backgrounds and light text
- **Light Theme**: Complete light theme variant with automatic adaptation
- **Proper Contrast**: Carefully balanced colors for accessibility in both modes
- **Responsive Design**: Optimized for both desktop and mobile viewing
- **Native Integration**: Works seamlessly with Obsidian's "Base color scheme" setting

### Light/Dark Theme System

The TailWind theme includes comprehensive support for both light and dark modes:

#### Automatic Theme Switching
- Uses Obsidian's native "Base color scheme" setting in Appearance preferences
- No manual theme switching required - follows your system preference
- Smooth transitions between light and dark modes

#### Smart Token Mapping
- **Dark Mode (.theme-dark)**: Uses light text on dark backgrounds
- **Light Mode (.theme-light)**: Uses dark text on light backgrounds  
- **Semantic Tokens**: All color mappings automatically adjust for optimal contrast
- **Drop-in Compatibility**: All color schemes work perfectly in both modes

#### Optimized Contrast
- Light theme uses darker color variants for better text readability
- Dark theme uses lighter color variants for comfortable viewing
- Shadows are adjusted for each theme (stronger in light, subtler in dark)
- Interactive elements maintain proper contrast ratios in both modes

### Obsidian Integration
- **Complete Variable Coverage**: All Obsidian CSS variables properly mapped
- **Semantic Token System**: Easy customization through two-layer variable architecture
- **Modern Interface**: Clean, minimal design that enhances content focus

## Architecture

The theme uses semantic tokens that map to Tailwind colors:
- **Background Tokens**: `--token-background-50` to `--token-background-950`
- **Text Tokens**: `--token-text-100` to `--token-text-900`
- **Spacing Scale**: `--token-space-0` to `--token-space-32`
- **Typography Scale**: `--token-text-xs` to `--token-text-7xl`

This allows theme-wide changes by updating semantic tokens while preserving access to the complete Tailwind color system.

### File Structure

TailWind Theme uses a modular structure for easier maintenance and customization:

- **theme-tokens.css**: Defines the design system foundation with colors, typography, spacing, and semantic mappings
- **theme-components.css**: Applies the token system to Obsidian UI elements and components
- **theme-utilities.css**: Contains utility classes for fine-tuning and customization
- **drop-ins/**: Ready-to-use theme enhancements and variations

### Drop-in Theme Variations

The theme includes ready-to-use variations in the `drop-ins/` folder:

1. **Color Schemes**:
   - `theme-stone-emerald.css`: Warm stone backgrounds with fresh emerald accents
   - `theme-zinc-amber.css`: Cool zinc backgrounds with warm amber accents

2. **UI Enhancements**:
   - `theme-rounded.css`: Adds more rounded corners to UI elements
   - `theme-interactive.css`: Enhances hover effects and animations

## Color Configuration Guide

The TailWind theme includes a sophisticated configurable color system based on Tailwind CSS color scales. You can easily customize your theme by choosing different color schemes for backgrounds and text.

### How It Works

The theme uses a systematic approach with semantic tokens:

#### Background Colors
- **Light Theme**: Uses lighter shades (50-200 range) from your chosen background color scheme
- **Dark Theme**: Uses darker shades (700-950 range) from your chosen background color scheme

#### Text Colors  
- **Light Theme**: Uses darker shades (700-950 range) from your chosen text color scheme
- **Dark Theme**: Uses lighter shades (100-500 range) from your chosen text color scheme

### Available Color Schemes

#### Background Options
- `slate` - Cool gray with subtle blue undertones
- `gray` - Pure neutral gray
- `stone` - Warm gray with brown undertones  
- `neutral` - Balanced gray (current default)
- `zinc` - Cool gray with subtle purple undertones

#### Text Options
- `blue` - Professional and trustworthy
- `emerald` - Fresh and energetic
- `amber` - Warm and inviting
- `red` - Bold and attention-grabbing
- `purple` - Creative and sophisticated
- `lime` - Fresh and vibrant (current default)
- `teal` - Calming and modern
- `orange` - Energetic and friendly

### Customizing Your Theme

You have several ways to customize the TailWind theme:

#### 1. Using Drop-in Files (Easiest)

Simply copy any of the drop-in CSS files from the `drop-ins/` folder to your `.obsidian/snippets/` folder and enable them in Obsidian's settings.

For example, to use the Stone + Emerald color scheme:

1. Copy `drop-ins/theme-stone-emerald.css` to `.obsidian/snippets/`
2. Enable it in Settings → Appearance → CSS snippets

#### 2. Creating Custom Color Schemes

You can create your own color combinations by making a CSS snippet in `.obsidian/snippets/`:

##### Example: Stone Background + Emerald Text

```css
/* Custom color scheme: Stone + Emerald */
:root {
  /* Update semantic tokens to use stone backgrounds */
  --token-background-50: var(--color-stone-50);
  --token-background-100: var(--color-stone-100);
  --token-background-200: var(--color-stone-200);
  --token-background-600: var(--color-stone-600);
  --token-background-700: var(--color-stone-700);
  --token-background-800: var(--color-stone-800);
  --token-background-900: var(--color-stone-900);
  --token-background-950: var(--color-stone-950);

  /* Update semantic tokens to use emerald text */
  --token-text-100: var(--color-emerald-100);
  --token-text-200: var(--color-emerald-200);
  --token-text-300: var(--color-emerald-300);
  --token-text-400: var(--color-emerald-400);
  --token-text-500: var(--color-emerald-500);
  --token-text-600: var(--color-emerald-600);
  --token-text-700: var(--color-emerald-700);
  --token-text-900: var(--color-emerald-900);
}
```

#### 3. UI Customizations

To customize the UI, you can combine color schemes with UI enhancements:

- **Rounded UI**: Use `theme-rounded.css` for softer, more rounded corners
- **Interactive Effects**: Use `theme-interactive.css` for enhanced hover effects

### Color Mapping Reference

#### Dark Theme Mappings
- **Primary Background**: `{scheme}-800`
- **Primary Alt Background**: `{scheme}-700`
- **Secondary Background**: `{scheme}-900`
- **Secondary Alt Background**: `{scheme}-950`
- **Normal Text**: `{text-scheme}-100`
- **Muted Text**: `{text-scheme}-200`
- **Accent Text**: `{text-scheme}-400`

#### Light Theme Mappings
- **Primary Background**: `{scheme}-50`
- **Primary Alt Background**: `{scheme}-100`
- **Secondary Background**: `{scheme}-100`
- **Secondary Alt Background**: `{scheme}-200`
- **Normal Text**: `{text-scheme}-900`
- **Muted Text**: `{text-scheme}-700`
- **Accent Text**: `{text-scheme}-600`

## Installation & Usage

1. **Activate Theme**: Settings → Appearance → Select "TailWind"
2. **Customize Colors**: Use drop-in files or create CSS snippets to override semantic tokens
3. **Preview Colors**: All colors follow the official Tailwind CSS color palette. Preview at: https://tailwindcss.com/docs/colors

### Advanced Customization

For advanced users who want more control:

1. **Component Styling**: Create a CSS snippet targeting specific Obsidian components
2. **Token Overrides**: Customize token values in your snippet to change colors, spacing, etc.
3. **Mix and Match**: Combine multiple drop-ins for a unique look

## Key Variables for Customization

### Main Token Categories
- **Colors**: `--token-bg-primary`, `--token-text-normal`, `--token-interactive-accent`
- **Spacing**: `--token-space-1` through `--token-space-32`
- **Typography**: `--token-text-xs` through `--token-text-7xl`
- **Radius**: `--token-radius-none` through `--token-radius-full`

### Component-Specific Tokens
- **Headers**: `--token-header-h1-size`, `--token-header-h1-bg`, etc.
- **UI Elements**: `--token-sidebar-item-padding-x`, `--token-tab-padding-y`, etc.
- **Interactive**: `--token-interactive-hover`, `--token-button-bg-hover`, etc.

Created by bears • Inspired by Tailwind CSS

<img width="946" alt="Pasted image 20220822145356" src="https://user-images.githubusercontent.com/693981/186000772-e689ecea-c3b7-4e9d-9204-7ad62c0123aa.png">

4. Click "Publish Release."
5. Make sure that `versions.json` is set up correctly. This file is a map.
  ```json
  {
    "1.0.0": "0.16.0"
  }
  ```
  
  This means that version 1.0.0 of your theme is compatible with version 0.16.0 of Obsidian. For the initial release of your theme, you shouldn't need to make any changes to this file.
 
### Steps for releasing new versions

Releasing a new version of your theme is the same as releasing the initial version.

1. From your theme's repository, click on "Releases."
2. On the Releases page, there should be a button to **Draft a new Release**. Press it.
3. Fill out the Release information form.
	- **Choose a Tag**: Type in the name of the version number here. At the bottom of the dropdown should be a button to create a new tag with your latest theme changes. Choose this option.
		<img width="333" alt="Pasted image 20220822145812" src="https://user-images.githubusercontent.com/693981/186000912-f494def9-0f67-4662-92bf-bd278082455f.png">
	- **Release Title**: This can be the version number.
	- **Description** _Optional_: Anything that changed
	- **Files:** The most important part of this form is uploading the files. You can do this by dragging 'n dropping the `manifest.json` file and the `theme.css` file your for theme inside the file upload field.

4. Click "Publish Release."
5. Update the `versions.json` file in your repository. For the initial release of your theme, you probably didn't need to make any changes to the `versions.json` file. When you release subsequent versions of your theme; however, it's best practice to include the new version as entry in the versions.json file. So this might look like:
  ```json
  {  
		"1.0.0": "0.16.0",
		"1.0.1": "0.16.0"
  }
  ```

  What's important to note here is: the new version is included as the "key" and the "value" is the minimum version of Obsidian that your theme compatible with. So if the new version of your theme is only compatible with an Insider version of Obsidian, it's important to set this value accordingly. This will prevent users on older versions of Obsidian from updating to the newer version of your theme.