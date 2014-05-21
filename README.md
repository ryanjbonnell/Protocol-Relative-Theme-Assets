# Protocol Relative Theme Assets

Transforms enqueued CSS and JavaScript theme URLs to use protocol-relative paths.

This plugin transforms any registered, enqueued CSS or JavaScript URLs into their "protocol-relative" equivalent.

Consider the following examples:

**Protocol Relative CSS URL**

`<link href="//example.com/wp-content/themes/twentytwelve/style.css" />`

**Protocol Relative Javascript URL**

`<script src="//example.com/wp-includes/js/jquery/jquery.js"></script>`

More appropriately called a "network-path reference" or "scheme-relative path", a protocol-relative URL helps to avoid common scenarios such as:

* Broken SSL padlock icon in browser's address bar when showing mixed HTTP/HTTPS content
* Error message in Internet Explorer saying, "This Page Contains Both Secure and Non-Secure Items"
* Serving HTTP assets when viewing HTTPS pages

The idea of using protocol-relative URLs was popularized by [Paul Irish](http://paulirish.com/2010/the-protocol-relative-url/) and has become common as sites switch between serving HTTP and HTTPS assets.

This plugin will standardize all properly enqueued theme files to use protocol-relative paths, even those added from third-party plugins.

_Note: This plugin does not transform any image paths that may be embedded in the WordPress editor or output as featured images or elsewhere in the theme -- it presently only works on enqueued CSS/JavaScript files._

## Changelog

### Version 1.0 (20 May 2014)

* Initial release
