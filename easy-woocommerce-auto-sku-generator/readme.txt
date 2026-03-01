=== Easy Auto SKU Generator for WooCommerce ===
Contributors: alexodiy, campusboy1987
Donate link: https://boosty.to/dan-zakirov/donate
Tags: woocommerce, sku generator, product sku, auto sku, variable product sku
Requires at least: 4.8
Tested up to: 6.9
Stable tag: 1.3.0
Requires PHP: 5.6
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Automatically generate SKU codes in WooCommerce with flexible formats, variation support, and bulk tools.

== Description ==
Generate WooCommerce SKU values automatically when creating products, editing products, or running bulk actions.

Easy Auto SKU Generator helps store owners keep SKU structure consistent without manual typing.

Tested with WordPress 6.9.1 and WooCommerce 10.5.2.

== Settings ==

WooCommerce &rarr; Settings &rarr; Products &rarr; SKU Settings

== Features ==

1. Auto-generate SKU for new products.
2. Skip generation when SKU already exists (unless recreate mode is enabled).
3. Generate variation SKUs for variable products.
4. Choose SKU format: numbers, letters, alphanumeric, or product slug.
5. Set SKU length.
6. Add prefix and suffix.
7. Add product ID to SKU.
8. Optional "Use Previous Product" mode (+1 sequence from previous product SKU).
9. Allow duplicate SKUs when needed.
10. Bulk generate SKU for all products.
11. Bulk generate SKU by category.
12. Additional number with configurable increment format.
13. Variation separator settings for variable products.

== Required Plugin ==

* [WooCommerce](https://wordpress.org/plugins/woocommerce/)

This plugin works only with WooCommerce.

== How it works ==

The plugin uses WooCommerce product meta (`_sku`) and applies your rules from SKU Settings.

You can use it in two modes:

1. **Product editor mode**: SKU is generated while creating or updating a product.
2. **Bulk mode**: SKU is generated for all products or selected categories.

When "Re-create existing SKUs" is disabled, only empty SKU values are generated.

== Bulk SKU Generation ==

Bulk generator supports:

* Generate SKU for all products.
* Generate SKU by category.
* Optional recreation of existing SKU values.
* Progress indicator during processing.

For large stores, run bulk generation in smaller batches to reduce server load.

== Translations ==

If you want to help with translations, please visit:
[translate.wordpress.org](https://translate.wordpress.org/projects/wp-plugins/easy-woocommerce-auto-sku-generator/)

== Installation ==

This section describes how to install the plugin and get it working.

Install From WordPress Admin Panel:

1. Login to your WordPress Admin Area
2. Go to Plugins -> Add New
3. Type "**Easy Auto SKU Generator for WooCommerce**" into the Search and hit Enter.
4. Find this plugin Click "install now"
5. Activate The Plugin

Manual Installation:

1. Download the plugin from WordPress.org repository
2. On your WordPress admin dashboard, go to ‘Plugins -> Add New -> Upload Plugin’
3. Upload the downloaded plugin file and click ‘Install Now’
4. Activate ‘**Easy Auto SKU Generator for WooCommerce**’ from your Plugins page.

== Frequently Asked Questions ==

= Can I contribute to the improvement of the plugin? =

Yes. Please share ideas or bug reports on the [support forum](https://wordpress.org/support/plugin/easy-woocommerce-auto-sku-generator/).

= Where can I find plugin settings? =

Open: WooCommerce &rarr; Settings &rarr; Products &rarr; SKU Settings.

= What SKU formats are available? =

You can generate SKU values using numbers only, letters only, alphanumeric format, or product slug.

= How do Prefix, Suffix, and Additional Number work together? =

Prefix is added at the beginning, suffix at the end, and additional number appends an incrementing numeric sequence in bulk generation.

= Does this plugin support variable products and variation SKU generation? =

Yes. The plugin can generate SKU values for variable products and variation items based on your current settings, including custom separators.

= What does "Re-create existing SKUs" do? =

When enabled, existing SKU values are replaced during bulk generation. When disabled, only products with empty `_sku` values are generated.

= What does "Use Previous Product" mean? =

This option creates the next SKU based on the last published product SKU (+1 logic). It is intended for sequential SKU workflows.

= Can I allow duplicate SKU values? =

Yes. You can enable duplicate SKU values in settings if your catalog workflow requires it.

= What batch size should I use for bulk SKU generation? =

For low-memory hosting, start with small batches (1-3 products per request). Increase batch size only if processing remains stable.

= Bulk SKU generation for all products stops and does not work correctly - what should I do? =

If bulk generation stops, first check the latest plugin version and server limits. See the related support topic [here](https://wordpress.org/support/topic/mass-creation-crashed/).

**What to check:**

1. Be sure to update the plugin to the latest version

2. Open browser DevTools on the settings page and check Console/Network for errors.

3. Check server logs for PHP or timeout errors and share details in the [support forum](https://wordpress.org/support/plugin/easy-woocommerce-auto-sku-generator/).

4. Contact your hosting support if you see memory, timeout, or HTTP 500 errors.

Please post the error details in the [support forum](https://wordpress.org/support/plugin/easy-woocommerce-auto-sku-generator/) so we can help faster.

== Screenshots ==

1. Format SKU
2. SKU Settings
3. Where to find the settings?
4. Support forum and field SKU
5. SKU generation options
6. Bulk generate SKU for all products
7. Bulk generate SKU by Category
8. Bulk generate SKU by Category
9. The process of generating SKU of all products
10. Completion of the SKU generation process for all products
11. Future plans

== Upgrade Notice ==

Version 1.3.0 improves reliability and performance for large catalogs: batch bulk generation, JSON-based processing, redesigned admin modal UI, and better SKU-field controls.

== Changelog ==

= 1.3.0 =
* Redesigned bulk generator modal dialogs in WordPress admin style.
* Added batch processing (1-10 products per request) for bulk SKU generation.
* Added "Recommend" button to suggest batch size based on server memory.
* Switched bulk processing responses from plain HTML to JSON.
* Refactored JavaScript modules to reduce global conflicts.
* Improved SKU field icon strip behavior and tooltip interactions.
* Improved "Take previous product" logic and internal code structure.
* Added HPOS (High-Performance Order Storage) compatibility declaration.

= 1.2.0 =
* Added new information to plugin settings.

= 1.1.9 =
* When editing or creating a product, a suffix is now appended.
* When editing or creating a product, the number specified in the "Additional number" settings is now added.

= 1.1.8 =
* Added High-Performance Order (HPOS) support
* Tested with the latest version of WooCommerce

= 1.1.7 =
* Update JavaScript settings
* Update readme
* Added subscription

= 1.1.6 =
* Update readme
* New donate link

= 1.1.5 =
* Tested compatibility with WordPress 6.3
* Tested compatibility with WooCommerce 8.0
* New readme
* The delimiter is now available when editing and adding a product
* Fixed re-creation of already existing SKU of a variant product

= 1.1.4 =
* Variant SKU customizations are now hidden in a separate group
* Preparing for global plugin update has been implemented
* Added "SKU suffix" option
* Added "Additional number" option
* Added "Format "Additional number" option
* Added "SKU suffix" option
* Added 2 formats for generating last numbers

= 1.1.3 =
* Tested compatibility with WordPress 6.2
* Tested compatibility with WooCommerce 7.9
* Added a setting for additional options in generating variant products.
* Added a setting for the separator in variant products when generating SKU.

= 1.1.2 =
* Tested compatibility with WordPress 5.9
* Tested compatibility with WooCommerce 5.8.3
* Changed SKU generator progress indicator
* Added style updates for SKU generator
* Added option "Allow identical SKUs"

= 1.1.1 =
* Added compatibility with the "Table Rate Shipping Method for WooCommerce by Flexible Shipping" plugin
* CSS class of the modal window is now unique. Added compatibility with other plugins

= 1.1.0 =
* Fixed bug with disabling SKU block

= 1.0.8 =
* Fixed an error generating variant products
* Changed the order of execution of the variable products generator script
* Fixed getting a basic SKU in relation to variable products in the SKU generator

= 1.0.7 =
* Fixed bug with SKU generation by slug of product

= 1.0.6 =
* Tested WP version 5.8

= 1.0.5 =
* Tested WP version

= 1.0.4 =
* Correction of error with number 0

= 1.0.3 =
* The limitation on the generation of the minimum number of characters has been removed

= 1.0.2 =
* Rename function "ffxf_action_javascript"

= 1.0.1 =
* Plugin tested with WordPress version 5.5

= 1.0.0 =
* Tested WP 5.4

= 0.9.9 =
* Fixed a bug that was caused due to duplication of SKU

= 0.9.8 =
* Update notice

= 0.9.7 =
* Added new functions "Bulk generate SKU by Category"
* Bugs fixed with the function of the previous product
* Take previous product has become more convenient
* Update CSS
* Update JS

= 0.9.6 =
* Update CSS
* Preparation for the introduction of a new parameter - Generation of SKU into separate categories.

= 0.9.5 =
* Fix error in notice

= 0.9.4 =
* Test WordPress 5.3

= 0.9.3 =
* Fixed bug with mass generation

= 0.9.2 =
* Re-create online button is now always available
* New support forum notification added

= 0.9.1 =
* WooCommerce test 3.8.0
* Optimize code
* Add notice

= 0.9.0 =
* fix translate and add text-domain in generate SKU

= 0.8.9 =
* update CSS

= 0.8.8 =
* fix translate

= 0.8.7 =
* Fixed translation strings
* Fixed translation selector

= 0.8.6 =
* fix missing dependencies ffxf_slug_script.js

= 0.8.5 =
* Now, after installing the plugin, you can immediately generate products without saving the general settings.
* New POT file
* Fixed text domain of the translation plugin

= 0.8.4 =
* Added and ready to use a new function "Bulk generate SKU for all products"
* New function “Bulk generate SKU by Category” prepared for implementation
* New function “Bulk generate SKU by Attributes” prepared for implementation
* New function “Bulk generate SKU by product tags” prepared for implementation
* New interface added

= 0.8.3 =
* Changed the main banner so as not to infringe on Woocommerce copyright
* In the latest version of plugin 0.8.3, preparations were made for implementing a function that generates SKUs for all products bulk. 

= 0.8.2 =
* Improved numerical value handling
* Fixed related edge-case errors

= 0.8.1 =
* Improved numerical value handling tests
* Added function for converting SKU numbers from previously published products
* Added notification for error and failure states

= 0.8.0 =
* Fix error id SKU and all option

= 0.7.9 =
* New feature refinement - "Consider the previous product"

= 0.7.8 =
* Improvement of the function "Consider the previous product"
* Fixed bugs with zeros
* Using the new function, the article can now be rewritten
* New styles added

= 0.7.7 =
* Add new functions "Take into account the previous product" 

= 0.7.6 =
* Product ID is now at the end SKU

= 0.7.5 =
* Fix JS error

= 0.7.4 =
* Fixed script connection

= 0.7.3 =
* Optimized code

= 0.7.2 =
* Fix JS error

= 0.7.1 =
* Fix error slug SKU

= 0.7.0 =
* Add new settings - Product Slug Generation
* Add Re-Create SKU online
* Optimized code

= 0.6.0 =
* Optimized settings code

= 0.5.0 =
* Fixed problems with literal values

= 0.4.0 =
* Added settings in ‘Woocommerce &rarr; Settings &rarr; Products &rarr; SKU Settings’
* Added option - Number of characters in SKU
* Added option - Prefix before SKU
* Added option - SKU format (Only numbers, Only letters, Letters and numbers)
* Added option - Use product ID in SKU
* Added option - Disable / Enable generation of SKU in variable goods
* Update generation function sku

= 0.3.0 =
* Update generation function sku

= 0.2.0 =
* Release
