# Narrative-Mod

This is a mod of Shopify's *Narrative* theme.  *Narrative-Mod* theme adds implementations for a bulk order page, a gift-wrapping option, a shipping calculator and an alternate product page.

## Bulk Order Page
The *Bulk Order* page is accessible from the menu. This page offers a quick way to add to the cart multiple products and variants from a collection.
Notable features:
- Responsive design using flexbox
- Support for items with variants composed of up to 3 options
- Support for items that do not have a variant
- Support for both the regular cart page and the cart drawer

![bulk-order](https://user-images.githubusercontent.com/4752832/29792516-a25db8f0-8c0e-11e7-94cb-516c8f0d784e.png)

## Gift Wrapping
Heavily modified version of Caroline Hill's [sample](https://github.com/carolineschnapp/carolineschnapp-gift-wrap/blob/master/gift-wrapping-multiple-charge.liquid) adding the following features:

- Support for both regular cart and cart drawer
- Support for two cost models (settable in theme's general settings): per-item and fixed-cost
- Auto adjustment of gift wrap item count when number of items in cart changes (applies to per-item cost model only)
- Auto removal of gift wrap item if all other items in cart are removed
- Autosave of gift-wrap note

![gift-wrap](https://user-images.githubusercontent.com/4752832/29792527-ad1a5a0a-8c0e-11e7-9b7b-39a8f1a37254.png)

## Shipping Calculator
Additional features and improvements from Caroline Hill's [sample](https://github.com/carolineschnapp/shipping-calculator/blob/master/shipping-calculator.liquid):
- Auto-saves of user-entered address into session storage upon leaving page.
- Restores user-entered address from session storage on cart page load.
- UX improvements:
     - Pressing ENTER on shipping form input fields does not perform a form submit (and page refresh), unless it's on the submit button
     - If ENTER was pressed on any input fields (except button) and the zipcode field is empty, move focus to zipcode field
     - Focus remains on the submit button, if the form submission was triggered from the said button
     - Highlights (with transition effects) and move focus on zipcode field if submitted zipcode was invalid
     - Highlight and coordinated transition effects of zipcode error message

![shipping-calculator](https://user-images.githubusercontent.com/4752832/29792531-aefc0166-8c0e-11e7-8d50-97de04497861.png)
     
## Alternate Product Page
Added features:
- Support for custom line item properties.
    - they can be added from Theme Editor
    - they can be set as "required" (or not) from the Theme Editor
    - their names can be customized from Theme Editor
    - their type (text, file, number, checkbox) can set from Theme Editor
    - For Type=number, the range can be set from Theme Editor
- Added a "quantity-in-cart" indicator showing the number of unit of the viewed product already in cart.

![alt-product-page](https://user-images.githubusercontent.com/4752832/29792535-b07cf7c0-8c0e-11e7-886f-0aff16b25b1b.png)

- - - 
#### Note
Some of these custom features may be better implemented if we had access to the un-minimized version of jquery.cart.js and theme.js.
