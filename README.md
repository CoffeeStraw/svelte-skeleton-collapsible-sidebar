# Svelte Skeleton Collapsible Sidebar

A plug-and-play collapsible sidebar component for Svelte 5 and Skeleton UI. This component provides a resizable and collapsible sidebar that can be positioned on any side of your application.

## Features

- 📱 Fully responsive and resizable
- 🎯 Supports all four positions (left, right, top, bottom)
- 🔄 Smooth collapse/expand transitions
- 🎨 Integrated with Skeleton UI theming
- ⚡ Lightweight and performant
- 💪 Written in TypeScript

## Installation

```bash
npm install svelte-skeleton-collapsible-sidebar
# or
yarn add svelte-skeleton-collapsible-sidebar
# or
pnpm add svelte-skeleton-collapsible-sidebar
```

## Usage

```svelte
<script>
  import CollapsibleSidebar from 'svelte-skeleton-collapsible-sidebar';
</script>

<CollapsibleSidebar>
  <!-- Your sidebar content here -->
</CollapsibleSidebar>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| `side` | `'left' \| 'right' \| 'top' \| 'bottom'` | `'left'` | Position of the sidebar |
| `minSize` | `number` | `150` | Minimum size in pixels |
| `maxSize` | `number` | `800` | Maximum size in pixels |
| `startSize` | `number` | `300` | Initial size in pixels |
| `collapsedSize` | `number` | `40` | Size when collapsed in pixels |
| `title` | `string` | `''` | Title shown when sidebar is collapsed |
| `isCollapsed` | `boolean` | `false` | Initial collapse state |

## Examples

### Basic Usage

```svelte
<CollapsibleSidebar side="left" title="Navigation">
  <nav>
    <ul>
      <li>Home</li>
      <li>About</li>
      <li>Contact</li>
    </ul>
  </nav>
</CollapsibleSidebar>
```

### Right-sided Sidebar

```svelte
<CollapsibleSidebar 
  side="right"
  startSize={250}
  minSize={100}
  maxSize={500}
  title="Settings"
>
  <!-- Settings content -->
</CollapsibleSidebar>
```

### Two-way Binding

```svelte
<script>
  let sidebarCollapsed = false;
</script>

<CollapsibleSidebar bind:isCollapsed={sidebarCollapsed}>
  <!-- Content -->
</CollapsibleSidebar>
```

## Styling

The component uses Skeleton UI's theming system and includes these default classes:
- `bg-surface-100-800-token` for background
- `border-surface-500/30` for borders
- `variant-soft` for the collapse/expand button

You can override these using Skeleton UI's theming system or by adding custom CSS.

## Requirements

- Svelte 5.0.0 or higher
- Skeleton UI

## License

MIT License - see [LICENSE](LICENSE) for details

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

If you encounter any issues or have questions, please file an issue on the [GitHub repository](https://github.com/CoffeeStraw/svelte-skeleton-collapsible-sidebar/issues).
