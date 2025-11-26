---
title: "Shortcode"
layout: "layouts/post.html"
permalink: /docs/webhotelier-for-wordpress/shortcode/
eleventyNavigation:
  key: Shortcode
  parent: WebHotelier for WordPress
  order: 3
---

## Shortcode
WebHotelier for WordPress can be used via shortcodes (or widgets/blocks).

Default shortcode:

```text
[wp-webhotelier]
```

Add the shortcode in the Classic editor, the Shortcode block in Gutenberg, or
use the PHP template code:

```php
<?php echo do_shortcode('[wp-webhotelier]'); ?>
```

All the shortcode arguments override the plugin defaults set in the admin menu.

Common arguments

1. `url` — example:

	```text
	[wp-webhotelier url="https://example.reserve-online.net"]
	```

	The `url` value should be the WebHotelier booking URL (ends with `reserve-online.net`).

2. `max-adults` — maximum number of adults (setting to `0` hides the field):

	```text
	[wp-webhotelier max-adults="5"]
	```

3. `max-children` — maximum number of children (use `0` to hide):

	```text
	[wp-webhotelier max-children="5"]
	```

4. `max-infants` — maximum infants (use `0` to hide):

	```text
	[wp-webhotelier max-infants="5"]
	```

5. `orientation` — layout. Options: `horizontal`, `vertical`, `fluid`.

	```text
	[wp-webhotelier orientation="fluid"]
	```

	- `fluid` is a safe default for content areas.
	- `horizontal` fits wide containers.
	- `vertical` works well for widgets/sidebars.

6. `checkout-date` — show checkout date selector instead of number of nights:

	```text
	[wp-webhotelier checkout-date="true"]
	```

7. `max-nights` — maximum nights (ignored if `checkout-date` is true):

	```text
	[wp-webhotelier max-nights="10"]
	```

8. `css-class` — add custom CSS classes to the form element:

	```text
	[wp-webhotelier css-class="my-class another-class"]
	```

9. `days-after-checkin-allowed` — delay for first available check-in day.

	- `0` allows booking for today, `1` allows booking from tomorrow, etc.
	- Default is `1`.

10. `opening-closing-dates` — define the hotel's open period using strict format
	 `YYYY-mm-dd to YYYY-mm-dd` (first = opening, second = closing). Examples:

	 ```text
	 [wp-webhotelier opening-closing-dates="2020-03-15 to 2020-10-20"]
	 [wp-webhotelier opening-closing-dates="2019-11-08 to 2020-03-18"]
	 ```

11. `display-blank` — open results in a new tab (1) or same tab (0):

	 ```text
	 [wp-webhotelier display-blank="1"]
	 ```

Notes

- If a setting is not provided in the shortcode it uses the plugin defaults from
  **WebHotelier Options** in the admin.
- The plugin automatically handles date ranges and will adjust years when
  necessary for `opening-closing-dates`.

