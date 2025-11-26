---
title: "Plugin Settings"
layout: "layouts/post.html"
permalink: /docs/webhotelier-for-wordpress/plugin-settings/
eleventyNavigation:
  key: Plugin Settings
  parent: WebHotelier for WordPress
  order: 5
---

## Plugin Settings
After activation, the plugin adds a **WebHotelier Options** admin menu where
you set plugin defaults used by shortcodes, widgets and blocks.

![WebHotelier Options Menu](/img/docs/WebHotelierOptionsMenu.png)

There are two main tabs in the options:

1. **Form Fields Settings** – set defaults for:
	 - `WebHotelier URL` (your hotel's `reserve-online.net` URL)
	 - `Max Nights`, `Max Rooms`, `Max Adults`, `Max Children`, `Max Infants`
	 - `Default Nights`, `Default Rooms`, `Default Adults`, `Default Children`, `Default Infants`
	 - `Days from today that Check-in is allowed`
	 - `Opening and Closing Dates` (supports `from` / `to` date ranges)

   **Note:** If your hotel closes in the next year, select the closing date accordingly:

   ![Different year opening closing dates](/img/docs/Opening-closing-dates-on-different-years.png)

2. **Form Customization Settings** – layout and appearance options:
	 - `Orientation` (horizontal, vertical, fluid)
	 - `Replace Nights with Checkout Date` (checkbox)
	 - `Open WebHotelier in new tab` (checkbox)
	 - `Calendar Date Format` (PHP date format string)
	 - `Custom CSS Class` (add classes applied to the form element)
	 - `Custom CSS` (code editor textarea to insert CSS rules)

Examples and screenshots (remote):

![Form Fields Settings](/img/docs/Web-hotelier-options-Form-Fields-Settings.png)
![Form Customization Settings](/img/docs/Web-hotelier-options-Form-Customization-Settings.png)

Notes

- The `WebHotelier URL` must be the URL assigned to your hotel by WebHotelier, e.g. `https://your-hotel.reserve-online.net`.
- If a numeric setting (like `Max Children`) is set to `0`, the corresponding
	field is hidden from the form.
- Opening/closing dates should be set with care; if the closing date is in the
	next year, set the year accordingly.
