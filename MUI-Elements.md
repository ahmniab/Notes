

# `CircularProgress`

> `CircularProgress` is a React component provided by Material-UI (MUI) that displays a circular progress indicator.

```tsx
<CircularProgress />
```

# `IconButton`

> `IconButton` in MUI (Material-UI) is a React component designed to render a clickable icon.

it used with close buttons like:

```tsx
return (
	<IconButton aria-label="close">
		<CloseIcon />
	</IconButton>
);
```

# `Typography`

> **The MUI Typography component is a pre-styled wrapper for text that ensures visual consistency and proper semantics across your entire application, all controlled from a central theme.**

## AI Side-by-Side Comparison

| | Using Raw `<h1>` | Using MUI `<Typography>` |
| :--- | :--- | :--- |
| **Consistency** | Hard to enforce; prone to style drift. | Enforced by a limited set of `variant` options. |
| **Semantics** | Locked to the tag. Hard to change. | Easily decoupled with the `component` prop. |
| **Theming** | Requires updating CSS in multiple files. | Change once in the theme, update everywhere. |
| **Maintenance** | Higher effort to maintain and scale. | Lower effort; the system manages itself. |
| **Functionality** | You must write all CSS yourself. | Comes with useful props like `gutterBottom` and `noWrap`. |


# `createStyles`

> When your styles rely on the MUI theme (e.g., accessing `theme.palette`, `theme.spacing`), `createStyles` is particularly useful.
> It creates a custom styles using global theme

# `BOX`

> The Box component is a generic container for grouping other components. It's a fundamental building block when working with MUI System—you can think of it as a `<div>` with extra built-in features, like access to your app's theme and the `sx` prop. 


```tsx
import * as React from 'react';
import Box from '@mui/system/Box';

export default function BoxBasic() {
  return (
    <Box component="section" sx={{ p: 2, border: '1px dashed grey' }}>
      This Box renders as an HTML section element.
    </Box>
  );
}

```

# `experimentalStyled`
`experimentalStyled` refers to an internal or outdated implementation of MUI's `styled()` utility, which has since been stabilized and is now simply `styled()`.

> The `styled()` utility is a feature inspired by libraries like styled-components , used to create new, reusable components with custom styles by wrapping existing components or HTML elements.

# `useMediaQuery`

> `useMediaQuery` in Material-UI (MUI) is a React hook that allows you to apply conditional logic and render different components or styles based on CSS media queries. It essentially provides a way to make your React components responsive to different screen sizes and device characteristics, similar to how CSS media queries work.

```tsx
const theme = useTheme();  const isMobile = useMediaQuery(theme.breakpoints.down('sm')); 
return (
    <div>
        {isMobile? (
		<p>This content is for mobile devices.</p> ) : (        
		<p>This content is for larger screens.</p> )}    
    </div>);

```

# `Tooltib`

> `Tooltip` is a component that displays informative text when a user hovers over, focuses on, or taps an element.

```tsx
<Tooltip title="Delete">
	<IconButton>
		<DeleteIcon />
	</IconButton>
</Tooltip>
```

# `Menu`

> the `Menu` component displays a list of choices on a temporary surface, appearing when a user interacts with a button or other control.

```tsx
<Menu
	id="demo-positioned-menu"
	aria-labelledby="demo-positioned-button"
	anchorEl={anchorEl}
	open={open}
	onClose={handleClose}
	anchorOrigin={{
	  vertical: 'top',
	  horizontal: 'left',
	}}
	transformOrigin={{
	  vertical: 'top',
	  horizontal: 'left',
	}}
>
	<MenuItem onClick={handleClose}>Profile</MenuItem>
	<MenuItem onClick={handleClose}>My account</MenuItem>
	<MenuItem onClick={handleClose}>Logout</MenuItem>
  </Menu>
```

# `Collapse`

> The`Collapse` component in Material-UI (MUI) is a transition component used to create smooth, animated expansions and collapses of content. You can use it to toggle the visibility of elements, such as showing more details within a card, expanding a list item, or animating rows in a table.

# `Chip`

> Chips allow users to enter information, mae selections, filter content, or trigger actions.

```tsx
// MUI Code
import * as React from 'react';
import Chip from '@mui/material/Chip';
import Stack from '@mui/material/Stack';

export default function BasicChips() {
  return (
    <Stack direction="row" spacing={1}>
      <Chip label="Chip Filled" />
      <Chip label="Chip Outlined" variant="outlined" />
    </Stack>
  );
}
```

# `Link`

> The MUI `Link` is a React component that styles and customizes the native HTML `<a>` (anchor) element, integrating it seamlessly with the MUI design system. It allows you to create styled hyperlinks for navigation, with full access to MUI's theming, typography, and styling props.

# `FormControl`

> `FormControl` is a wrapper component in MUI that provides context for form inputs, such as their state, size, and styling.

# `FormHelperText`

> `FormHelperText` is a Material-UI (MUI) component used to display a small block of text below form controls like text fields, select inputs, or checkboxes.

```tsx
<FormControl error={isError}>
	<TextField 
		label="Username"
		value={username}
		onChange={(event) => setUsername(event.target.value)}
		aria-describedby="username-helper-text"
	/>
	<FormHelperText id="username-helper-text">
		{isError ? 'Username must be at least 5 characters long.' : 
		'Choose a unique username.'}
	</FormHelperText>
</FormControl>
```


# NOTE
**I used AI to help me in this document**

# Resources
https://mui.com/material-ui/react-typography/ <br>
https://m2.material.io/design/typography/the-type-system.html#type-scale <br>
https://mui.com/system/react-box/ <br>
https://www.styled-components.com/ <br>
https://mui.com/material-ui/react-chip/
