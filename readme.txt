=== WP Approve User ===
Contributors: kobenland
Tags: admin, user, login, approve, user management, plugin
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=G65Y5CM3HVRNY
Requires at least: 3.1
Tested up to: 3.3.1
Stable tag: 2.0.0

Adds action links to user table to approve or unapprove user registrations.

== Description ==

This plugin lets you approve or reject user registrations.
While a user is unapproved, he/she can't access the WordPress Admin.

On activation of the plugin, all existing users will automatically be flagged Approved. The blog admin will never experience restricted access and does not need approval.

= Translations =

I will be more than happy to update the plugin with new locales, as soon as I receive them!
Currently available in:

* Deutsch
* English


== Installation ==

1. Download WP Approve User.
2. Unzip the folder into the `/wp-content/plugins/` directory.
3. Activate the plugin through the 'Plugins' menu in WordPress.
4. Make sure user registrations is enabled in 'General Settings'.


== Frequently Asked Questions ==

= Once a new user has been approved, will the plugin send out an email to inform them they have been approved? =

No. (At least not yet.) But with Version 1.1.0 developers can hook into the `wpau_approve` and `wpau_unapprove` action hooks and use them to send out emails.


= Plugin Hooks =

**wpau_approve** (*int*)
> User-ID of approved user

**wpau_unapprove** (*int*)
> User-ID of unapproved user


== Screenshots ==

1. Error message when user is not yet approved.
2. Row action when user is approved
3. Row action when user is not yet approved
4. Count notification and row highlight for unapproved users


== Changelog ==

= 2.0.0 =

* Optimized alteration of Users menu item. Props Rd

= 1.1.1 =
* Fixed a bug, where the call to action bubble didn't account for newly registered

= 1.1.0 =
* Added bulk action for approving and unapproving users
* Added notification of unapproved users in admin menu item (WordPress 3.2+)
* Added highlight of unapproved users
* Added action hooks on (un-)approval. See hook reference
* Users created by an Administrator will automatically be approved
* Updated utilities class
* Now an instance of the Obenland_Wp_Approve_User object ist stored in a static property to make deregistration of hooks easier.

= 1.0 =
* Initial Release


== Upgrade Notice ==