=== JBlog Captcha ===
Contributors: alonelion1987
Official website: https://zharikov.site/kapcha-v-polzovatelskix-formax/
Tags: anti-spam, antispam, anti-spam security, captcha, custom form captcha, symbol captcha, security custom form, custom captcha, capcha, develop captcha, kit captcha, login captcha
Requires at least: 4.2
Tested up to: 4.9.1
Stable tag: 1.4.4
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Сaptcha generated numbers and latin characters. Designed for use in custom forms and displays a simple shortcode, and connect to log form.



== Description ==

JBlog Captcha generates a picture with the characters and the text box. It is possible to choose the background for the image, change the font color and change count symbols in captcha.

This plugin will be an indispensable tool for developers of custom forms.

The documentation provided with comprehensive information on the methods of treatment of user data sent to the server.

Version 1.4.1 captcha automatically connects to the login form admin.

[Official plugin page](https://zharikov.site/kapcha-v-polzovatelskix-formax/)
[Example ajax- feedback forms on the basis of this plugin](https://zharikov.site/sozdaem-ajax-kontakt-formu-v-wordpress/)



== Installation ==

1. Activate the plugin through the "Plugins" menu in WordPress.
2. Go to setting `settings/JBlog Captcha` page and change the default settings.



== Frequently Asked Questions ==

= How do I display the form online captcha =

You have to use shortcode to check: `<?php if(class_exists('JBlogCaptcha')){print do_shortcode("[jbcptch]");} ?>` or just `[jbcptch]` in editor WordPress

= What functions can I use the test to check if the user entered the captcha or not? =

The file handler on the server side, you must define the variable `$ _POST ['str']`, which you pass the captcha value entered by the user;
In the file - handler: the condition before `... if () {}`, in which the check data, use the instructions: `JBlogCaptcha::instance()->chekSession();`, which checks whether the correct CAPTCHA introduced;
In the file - handler: in the condition `if (var_1 && var_2 && ...) {}`, use the instructions: `JBlogCaptcha::instance()->getChek()`, which returns true if the CAPTCHA is entered correctly , along with a test of its own data;

= What should I bring shortcode `[jbcptch]` =

This shortcode will return the html generated image with symbols and text field



== Screenshots ==

1. Admin panel settings page.
2. Captcha concluded in the public section.
3. Captcha in login form.



== Changelog ==

= 1.4.3 version (11.01.2016) =
UPDATE: removed one function GD-lib, representing a solution to unsafe platforms Debian standard extension for PHP, GD-lib, gd.so.

= 1.4.2 version (23.12.2015) =
UPDATE: Fixed a bug with the ability to login to the admin panel from the first time.

= 1.4.1 version (18.12.2015) =
ADDED: Captcha connected to login form.

= 1.3.1 version (17.12.2015) =
UPDATE: Improved script generation image, the image is displayed is now always up to date as to bypass the browser cache. Testing in IE excellent results!
ADDED: removed unreadable characters and adds the ability to choose between 2-3, 3-4, 4-5 characters.

= 1.2.3 version (12.05.2015) =
ADDED: put case sensitive captcha

= 1.1 version (09.05.2015) =
UPDATE: Optimized code and removed unnecessary functions
ADDED: A larger selection of characters and added ability to change the number of characters

= * 1.0 version of the repository =



== Upgrade Notice ==

1.0 version start
