# Bison Example Theme

This demo website is an example of how you can use [Statamic](http://statamic.com) and [Bison](https://builtwithbison.com) to create a simple ecommerce website.

It definitely does _not_ show all the features of Bison. For full documentation, visit the [Bison website](https://builtwithbison.com/docs).

Feel free to use this as a starting point for your own site, or as a learning tool.  
It should _not_ be used as-is.



## Installation

1. Install a copy of Statamic as per the [documentation](http://statamic.com/learn/installing-and-updating/installing).
2. Install a copy of Bison as per the [documentation](https://builtwithbison.com/docs/getting-started/installing-and-updating).
3. Replace the `_content` directory.
4. Copy across `_themes/bison_example` and change the `_theme` setting to `bison_example`.
5. Replace the `assets/img` directory.
6. Replace the `_config/fieldsets` directory.
7. Copy across `_config/routes.yaml` (or amend to the existing file).
8. Ensure `1-products`, `_content/orders` and `_discounts` are writeable.
9. To access Bison's CP area, append `bison: true` to `_admin_nav` in `settings.yaml`.



## Support

* If there's an issue with the theme itself, please open an issue in this Github repo.
* If you have general how-to about Bison, open a ticket in [support](http://support.builtwithbison.com).

<br>

---

<br>

## About the theme

### Product types
Products are split into separate folders to demonstrate different usage examples.

* "Simple" products have either no options or they use a basic grid field to specify a single set of basic price modifiers. A single stock level can be managed for the entire product.
* "Complex" products contain the product option matrix fieldtype, which allows them to have multiple sets of options and price modifiers, each of which get their own stock level.
* A "Variable price" product is one where the user is able to choose the price. There is only one on here, and it's the [donation](/donation).

You can view the content md files and/or the fieldsets to get a better understanding.

### Tax
The `tax_rate` has been set to 10%.  
The donation product has been marked as 'tax free'.

### Shipping
The shipping method is `multiple_flat_rate` with two options.  
You can choose from the flat rates on the checkout/shipping page.

### Checkout
The `Dummy` gateway is used for checking out.  
If you want to use `Stripe`, there are partials in `templates/checkout_3` and `layouts/default` ready to be swapped out. You'll need to add your private API key to `bison.yaml` and your public key to the javascript partial.

### Control Panel
The orders and discounts folders have been hidden from the 'Pages' tab in the CP. You can access these through the "Store" section.