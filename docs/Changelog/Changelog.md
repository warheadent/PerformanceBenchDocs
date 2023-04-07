# Changelog

Releases are designated as simple version numbers. Any hotfixes will still be considered part of the same "version" when an update is pushed.

### V3
*Release pending
Versions: 5.0, 5.1, 5.2

This release adds and improves on nearly every aspect of the plugin. With this release, we're sunsetting 4.27 support since this update was produced within 5.0 and Unreal doesn't handle binary backwards compatibility that well. If there is significant need for a 4.27 backport, let me know.

5.2 support for this release is also planned once the version exits preview testing.

- **NEW:** Color Themes
	- This update ships with 6 different color themes, as well as an option for you to select your own color that you prefer
- **NEW:** Structured data ready for export
	- With the initial release, there were plans to allow for users to be able to export test result data but there wasn't anything set up to allow developers to hook it into their own solutions. With this update, we provide a results data structure that supports this
- **NEW:** GPU Driver Version and Date reporting
	- This release exposes the user's driver version and driver date (if reported by the system) to the developer. This was planned for the initial release of the plugin but ended up getting cut due to time constraints and issues with getting the plugin to compile
- **NEW:** FPS counter next to Score widget
	- This can be toggled within the Test Manager
- **NEW:** Submit Data
	- We restored this button since we expect developers to override the Submit Data event in Blueprint and hook in their own functionality for either exporting data to CSVs or posting to graph sites
	- By default, it just prints a simple test results string to the log
	- Visibility to the button can be controlled by the Test Manager

- **IMPROVED:** Most developer-exposed functions now have descriptions and proper categorization
- **IMPROVED:** Frame Graph (how we determine average, min and max FPS values) is now way more accurate than before
- **IMPROVED:** Exit to Menu button now is overridable
	- We shipped this to always quit the application and that was not the intent. While it still does this by default, you can override the blueprint event to hook into your own logic.
- **IMPROVED:** Score Grades now reference a string table instead of individual localized texts
	- Score grading (poor, great, excellent, etc.) now reference a String Table asset
	- We'll continue to improve on this aspect of the plugin to make this friendlier to developers and end-users.

- **FIXED:** Score Grader Slider accuracy
	- There was an issue where the slider (the arrow underneath the grades at the end result screen) wasn't accurately lining up with the grade that a user got. The logic here has been redone and it should hopefully always get the result correct.



### V2
*Released 12/1/2021*

This release is focused on smaller quality of life updates. Other upcoming features are still in the pipeline.

- **NEW:** Camera fades when beginning and completing the benchmark sequence
	- Duration fades can be customized via the Test Manager under Setup > Sequence
- **NEW:** Customize the More Details text on the Test Results widget via Test Manager

### V1
*Released 11/28/2021*

Official marketplace release.