=== Advanced Browser Check ===
Contributors: darkwhispering
Donate link: http://darkwhispering.com/by-me-a-beer
Tags: firefox, chrome, opera, safari, internet explorer, ie6, ie7, ie8, ie, ff, plugin, browser, block browser, block ie6, browser check, check, popup, warning, old, old browser, stop, stop ie, block internet explorer, browscap
Requires at least: 3.0.0
Tested up to: 4.0.0
Stable tag: 4.0.2

Tell IE users to change browser? Or is your site for Chrome only? Now you choose what browsers should trigger a warning popup or not on your site.

== Description ==

**This plugin requires PHP 5.3 or above**

This plugin give you the option to give a visitor of your site a warning popup if they use a browser that you don't support. For example, Internet Explorer 9 or lover.

It supports the 5 largest and most popular browser on the market.

* Firefox
* Chrome
* Safari
* Opera
* Internet Explorer

You can customize the warning message, choose what browsers download pages you want to display a link to, select what browsers and browser versions that should trigger the popup and if the user can or can't hide the popup.

If you allow users to hide the popup, a cookie is set that expires after 24h. After 24h, the user will see the popup again with the option to hide it for another 24h.

This plugin is tested and works with the WP Super Cache and W3 Total Cache plugins. It is also tested and working on Wordpress Networks.

**If you run into problems, please check the [FAQ](http://wordpress.org/plugins/advanced-browser-check/faq/). If you don't find and answer there, look in the [support section](http://wordpress.org/support/plugin/advanced-browser-check) if anyone else have/had the same isssue and if it has been resolved. Creating a new support ticket should always be your last resort for help. Thanks.**

*There is versions added of browsers that it not yet released as stable versions. This is to minimize the need of an plugin update in the future when new browsers are released and to let users try the plugin with beta and alpha version of the browsers browsers. I will do my best to keep this plugin updated with the latest versions of available browsers.*

== Installation ==

1. Upload the zipped file to yoursite/wp-content/plugins
2. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= I get "Fatal error: Allowed memory size of 67108864 bytes exhausted..." =

This plugin can be a little heave the first time it is running, when creating the configuration and cache files. If you see a memory error like this it means the plugin are trying to use more memory then it is allowed to. The solution is simple though, bump up the limit.

You might need to contact your hosting provider to help you, or follow [this](http://bestphphosting.net/how-to-increase-php-memory-limit/) or [this](http://www.devtnt.co/how-to-increase-php-memory-limit-on-godaddy-hosting/) guide.

= I get "Parse error: syntax error, unexpected T_STRING, expecting T_CONSTANT_ENCAPSED_STRING..."  =

If you see a PHP error similar to this, that means you have a PHP version below 5.3. The plugin uses PHP Namespaces and PHP 5.3 is required as minimum. Please contact your hosting company and let then know you need PHP upgraded.


= I see a 404 error in the console =

For some users, that have a very secure setup of Wordpress can get this issue if they block direct access to plugin files. See [this support thread](http://wordpress.org/support/topic/failed-to-load-resource-404-advanced-browser-checkphp) for information and direcation of what might be the cause of your issue.

= There is nothing! No overlay, no popup =
The plugin requires that your theme have the wp_footer() function added. Without this, the plugin can't create the code it needs to place the overlay and popup on your site.

You also need to have wp_head() function added in your theme header for the script and stylesheet files.

= I only get a black overlay, no popup =
You can get this for many reasons. It can be any of the plugins you have installed that is not compatible with my plugin. It can also be your theme.

I test the plugin before every update on a clean Wordpress installation with no other plugins activated or custom theme installed. Due to the large amount of 3rd party themes and plugins for Wordpess, it is impossible to guarantee that the plugin will work with them all.

Before posting a support thread, please try to inactivate all your plugins except Advanced Browser Check and try again. If you still have the issue, try with another theme, or install a clean Wordpress is a subfolder so you can test the plugin on your server with a clena Wordpress installation.

= I have selected not to block Chrome (or any other browser), but I still get the overlay =
Please read the above answer and perform the same tests before you start a new support thread. You should also turn on debugging so you see what browser the plugin detects you are using.

= I have performed all test above, still not working =
Okay, might be time to start a support thread, but first, please see if someone else have had your issue and see if they might found a solution before you start a new thread.

If you create a new support post, please provide as much info as possible. Like what Wordpress version you have, version of the plugin, browser you tested and versions on those browser. And of course, any error messages you see if you have that.

== Screenshots ==

1. Frontend screenshot
2. Backend screenshot

== Upgrade Notice ==

= 3.0.0 and above =
Version 3+ includes a lot of improvments and a complete rewrite to make the plugin better and more stable.

== Changelog ==

= 4.0.2 =
* Fixed issue where some Chrome and Safari browsers got detected as Internet Explorer on Windows platforms.

= 4.0.1 =
* Added missing jquery dependency to wp_enqueue_script

= 4.0.0 =
* Reverted back from Browscap, it gave more problems and issues then it solved.
* Fixed issue reported with Google Chrome 38. Thanks for all the feedback.
* The move away from Browscap will solve the memory issue some users are experience.
* Updated the list of browsers that can be blocked.
* Plugin is now also much faster, Browscap were really heavy to load.

= 3.1.0 =
* Updated browscap to utilize less memory.
* Added local default broscap.ini.
* Added local pre-cached cache file to minimize memory usage more.
* Moved cache folder into the plugin folder
* Updated browscap.php to 2.0 from 2.0b
* Tested on Wordpress 4

= 3.0.3 =
* The plugin are now doing AJAX calls "correctly" using the wp_ajax action hook. Hoping this will solve the issue with plugin_dir_path() not working for some users.

= 3.0.2 =
* Replaced the use of WP_PLUGIN_DIR with plugin_dir_path() function.

= 3.0.1 =
* Prefixed core files to minimize risks of conflicts with other plugins.

= 3.0.0 =
* Rewritten and now using [PHP Browscap library](https://github.com/GaretJax/phpbrowscap) for browser detection.
* Updated browser versions. Includes current versions plus 5 future and 10 past versions.
* Plugin now REQUIRES a cache folder located in /wp-content/cache with full read and write permissions.
* Added a debug option for easier debuging.
* New cleaner design of the overlay.
* Better responsivness of the overlay, should not be a problem to close it on mobile devices.
* Smaller browser icons.
* General bug fixes and tweaks

= 2.2.0 =
* Added fix for problems with enqueue loading of scripts and css styles. Thanks @sireneweb for the fix.
* Moved hide link to top right corner.
* Minor style changes to the overlay box.
* Added browser names below browser icons.
* updated screenshots

= 2.1.3 =
* Updated list of browser versions
* Tested on Wordpress 3.6

= 2.1.2 =
* Fixed small error with the post ajax variable triggering error when empty or not existing.

= 2.1.1 =
* Hotfix: bug in the check for iOS devices

= 2.1.0 =
* Browser icon links now open in new tab/window
* Popup will no longer show up when the browser is unknown or not one of the supported
* Popup will NOT show up on iOS devices (iPhone & iPad) or Android devices
* Updated and removed browser version numbers on settings page

= 2.0.2 =
* Plugin tested and now working on Wordpress Networks

= 2.0.1 =
* Fixed problem with default values not beeing loaded on a fresh plugin installwith no records in the wp option table

= 2.0.0 =
* Large part of the plugin is re-written
* the .json file ir removed and replaced with a php function in the init.php
* Better commenting in the code
* Removed screenshots from the plugin folder, no need for them to be dl with the plugin
* New layout of the settings page, now more streamlined with the Wordpress admin
* Popup now looking good in IE 6 to 9
* Added option to not block a browser at all.

= 1.0.2 =
* Fixed problem with popup not beeing displayed properly in IE6

= 1.0.1 =
* Fixed problem with browser select boxes not shownig up.

= 1.0.0 =
* Initial release
