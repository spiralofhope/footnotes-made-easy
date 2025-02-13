=== Footnotes Made Easy ===
Contributors: lumiblog, dartiss
Tags: bibliography, footnotes, formatting, reference
Donate link: https://wpcorner.co/donate
Requires at least: 4.6
Tested up to: 6.5
Requires PHP: 7.4
Stable tag: 3.0.3
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Allows post authors to easily add and manage footnotes in posts.

== Description ==

Footnotes Made Easy is a simple, but powerful, method of adding footnotes to your posts and pages.

**Key features include...**

* Simple footnote insertion via double parentheses
* Combine identical notes
* Solution for paginated posts
* Suppress Footnotes on specific page types
* Option to display ‘pretty’ tooltips using jQuery
* Lots of configuration options
* And much, much more!

**Footnotes Made Easy is a fork of [WP Footnotes](https://github.com/drzax/wp-footnotes "Github - wp-footnotes"), a plugin by Simon Elvery which was abandoned some years ago**.

**Please visit the [Github page](https://github.com/wpcorner/footnotes-made-easy/ "Github") for the latest code development, planned enhancements and known issues**.

== Getting Started ==

Creating a footnote is incredibly simple - you just need to include your footnote in double parentheses, such as this...

This is a sentence ((and this is your footnote)).

The footnote will then appear at the bottom of your post/page.

**Important note:** Make sure you include a space before your opening double parentheses or the footnote won't work!

== Options ==

You have a fair few options on how the identifier links, footnotes and back-links look which can be found in the WordPress admin area under 'Settings -> Footnotes'.

== Paginated Posts ==

Some of you seem to like the paginating post, which is kind of problematic. By default, each page of your post will have its own set of footnotes at the bottom and the numbering will start again from 1 for each page.

The only way to get around this is to know how many posts are on each page and tell Footnotes Made Easy what number you want the list to start at for each of the pages. So at some point on each page (that is, between each `<!--nextpage-->` tag) you need to add a tag to let the plugin know what number the footnotes on this page should start at. The tag should look like this `<!--startnum=5-->` where "5" is the number you want the footnotes for this page to start at.

== Referencing ==

Sometimes it's useful to be able to refer to a previous footnote a second (or third, or fourth...) time. To do this, you can either simply insert the exact same text as you did the first time and the identifier should simply reference the previous note. Alternatively, if you don't want to do all that typing again, you can construct a footnote like this: `((ref:1))` and the identifier will reference the footnote with the given number.

Even though it's a little more typing, using the exact text method is much more robust. The number referencing will not work across multiple pages in a paged post (but will work within the page). Also, if you use the number referencing system you risk them identifying the incorrect footnote if you go back and insert a new footnote and forget to change the referenced number.

== Available in 8 Languages ==

Footnotes Made Easy is fully internationalized, and ready for translations.

**Many thanks to the following translators for their contributions:**

* [David Artiss](https://profiles.wordpress.org/dartiss/), English (UK)
* [Mark Robson](https://profiles.wordpress.org/markscottrobson/), English (UK)
* [Annabelle W](https://profiles.wordpress.org/yayannabelle/), English (UK)
* [maboroshin](https://profiles.wordpress.org/maboroshin/), Japanese
* [Laurent MILLET](https://profiles.wordpress.org/wplmillet/), French (France)
* [B. Cansmile Cha](https://profiles.wordpress.org/cansmile/), Korean 
* [danbilabs](https://profiles.wordpress.org/danbilabs/), Korean
* [denelan](https://profiles.wordpress.org/danbilabs/), Dutch 
* [Peter Smits](https://profiles.wordpress.org/psmits1567/), Dutch
* [Pieterjan Deneys](https://profiles.wordpress.org/nekojonez/), Dutch (Belgium)
* [Alex Grey](https://profiles.wordpress.org/alexvgrey/), Russian

**If you would like to add a translation to this plugin then please head to our [Translating WordPress](https://translate.wordpress.org/projects/wp-plugins/footnotes-made-easy "Translating WordPress") page**

== Installation ==

Footnotes Made Easy can be found and installed via the Plugin menu within WordPress administration (Plugins -> Add New). Alternatively, it can be downloaded from WordPress.org and installed manually...

1. Upload the entire `footnotes-made-easy` folder to your `wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress administration.

Voila! It's ready to go.

== Frequently Asked Questions ==

= How do I add a footnote to my post or page? = 

To add a footnote, surround the footnote text with the opening and closing footnote markers specified in the plugin settings. By default, these are `(( and ))`.

= Other than the available options, can the footnotes output be styled? =

Yes, it can. The easiest way is to use the CSS editor in your theme customizer. For example, 'ol.footnotes' refers to the footnotes list in general and 'ol.footnotes li' the individual footnotes.

= Can I disable footnotes on specific parts of my website? =

Yes, the plugin provides options to disable footnotes on the home page, archives, search results, feeds, and previews.

== Screenshots ==

1. The Settings screen with advanced settings shown
2. Continuation of the settings screen with advanced settings shown
3. The post editor page showing how to insert footnotes
4. Live preview of a post page showing footnotes within the page
5. Live preview of a post page showing the list of footnotes at the bottom of the post

== Change Log ==

I use semantic versioning, with the first release being 1.0.

= 3.0.3 =
* Maintenance: Updated README to grammatically correct the content.
* Maintenance: PHP 8.2 Compatibility test passed.
* Maintenance: AD UI Box added to the plugin's settings/options page.

= 3.0.2 =
* Maintenance: Updated this README to include the new contributor, and more FAQs. Also updated the image assets (banner and icon)

= 3.0.1 =
* Maintenance: Removed all the adoption notices.

= 3.0 =
* Maintenance: Re-release of v1.0.4, to replace the updates added by another developer.

= 1.0.4 =
* Bug: Well, I messed that release up and left some test dates in place. Apologies. This fixes it all now.

= 1.0.3 =
* Maintenance: Added notices about the plugin closure

= 1.0.2 =
* Bug: Fixed some bugs around settings getting saved (thanks to [Rufus87](https://wordpress.org/support/users/rufus87/))
* Enhancement: Improved code to better meet VIP coding standards (not 100% yet but looking better!)
* Enhancement: Added Github links to plugin meta. Added other useful meta as well
* Enhancement: Minor enhancements to the way that field headings are shown in the settings
* Enhancement: Added a further check to the settings savings function, to ensure it's not called when it's not needed (thanks to [seuser](https://wordpress.org/support/users/seuser/))
* Maintenance: Increased minimum PHP level 5.6 after reports of issues at 5.4. Upgrade people!
* Maintenance: Removed some redundant code from where there used to be a button on the settings screen to reset all the options

= 1.0.1 =
* Maintenance: Updated this README to display better in the new plugin repository. Also updated the image assets (banner and icon)
* Maintenance: Minimum WordPress requirement is now 4.6. This means various checks and bits of code could be removed, including the languages folder, as this is now handled natively.

= 1.0 =
* Initial release

== Upgrade Notice ==

= 3.0.3 =
* Maintenance: Updated readme text, added AD UI Box. 
