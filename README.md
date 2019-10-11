# SearchDigest
MediaWiki extension which tracks failed searches on your wiki and displays them on a dedicated special page. This was originally a feature on Wikia wikis.

**Live demo**: https://runescape.wiki

## Requirements
- **MediaWiki 1.31+**

## Installation

1. Clone this repository to your MediaWiki installation's `extensions` folder
2. Run the `maintenance/update.php` update script to add the necessary tables to your database
3. Modify your `LocalSettings.php` file and add:

```php
// Load the extension
wfLoadExtension( 'SearchDigest' );
```

## Configuration
| Variable | Type | Description | Default |
| --- | --- | --- | --- |
| `$wgSearchDigestSafe` | bool | Whether to wrap some extension functionality in try/catch statements to avoid breaking Special:Search if something goes wrong | `true`
| `$wgSearchDigestStrikeValidPages` | bool | Whether to strike out valid pages (pages that exist) on the special page | `true`
| `$wgSearchDigestCreateRedirect` | bool | Whether to show a button for quickly creating redirects on Special:SearchDigest (requires JS in browser) | `true`

## Translation
This extension can be translated through the messages in the `ì18n` folder if you're a developer. As a wiki administrator, you may find it a better option to edit the messages on-site in the MediaWiki namespace.

## License
This extension is licensed under GNU GPLv3, [see here](LICENSE) for more information.