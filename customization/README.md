# OWASP Juice Shop - Customization Tutorial

## Prerequisites

1. [Install OWASP Juice Shop](https://github.com/juice-shop/juice-shop#setup) locally. 
2. Copy all `.yml` files from this folder into the `/config` folder of your local Juice Shop installation.
3. Open [OWASP Juice Shop - Tutorial Series - Customization.pdf](OWASP%20Juice%20Shop%20-%20Tutorial%20Series%20-%20Customization.pdf) for context and general instructions.

## Tutorial Steps

### 1. Name and Logo
```
NODE_ENV=01-name_and_logo npm start
```
Custom name and logo appear at the top left of every screen in the application.

### 2. Welcome Banner 
```
NODE_ENV=02-welcome_banner npm start
```
Delete all cookies of the application, then refresh your browser to see the customized welcome banner. 

### 3. No Banner 
```
NODE_ENV=03-no_banner npm start
```
Delete all cookies of the application, then refresh your browser. The welcome banner no longer appears.

### 4. Theme and Cookies 
```
NODE_ENV=04-theme_and_cookies npm start
```
Delete all cookies of the application, then refresh your browser. You will notice the changed color palette and also the customized and themed cookie banner in the right lower corner.

### 5. Social Links
```
NODE_ENV=05-social npm start
```
Visit the _About Us_ page to see your overwritten social links.

### 6. Emails
```
NODE_ENV=06-emails npm start
```
Visit the _About Us_ page to find the authors of all pre-existing feedback now have the custom email. Open any product with a user review to see the same effect.

### 7. Favicon
```
NODE_ENV=07-favicon npm start
```
You should see your custom favicon in your browser tab.

### 8. Notifications off
```
NODE_ENV=08-notifications_off npm start
```
This config change is supposed to hide notifications and confetti from solved hacking challenges. But this config contains a small schema error you need to fix.

### 9. Schema validation
```
NODE_ENV=09-schema_fixed npm start
```
The schema is now valid again. When you solve a hacking challenge, you no longer see the notification banner. Also, the confetti cannon no longer fires.

### 10. First product
```
NODE_ENV=10-single_product npm start
```
In this config you defined your first own product. When configuring own products, they replace the original product inventory. This leaves some challenges impossible to solve, which is reported as validation errors in the config.

### 11. Default challenge products
```
NODE_ENV=11-default_challenge_products npm start
```
The quickest way to get back to a working configuration, is to add back all original products from `default.yml` which were needed for hacking challenges. When starting the Juice Shop, you now see some of these plus your own original product.

### 12. Product Tampering Challenge
```
NODE_ENV=12-product_tampering_challenge npm start
```
This increment replaces the default product for the _Product Tampering_ challenge with a custom one.

### 13. Christmas Special Challenge
```
NODE_ENV=13-christmas_special_challenge npm start
```
This increment replaces the default product for the _Christmas Special_ challenge with a custom one. Please note that this product is not visible because it is soft-deleted due to no longer being available. On the surface you see no difference between a Juice Shop started with this or the previous config. 

### 14. More Products w/ reviews
```
NODE_ENV=14-more_products_with_reviews npm start
```
You will see a few more products on the main screen now, making the shop feel a lot less empty. 

### 15. Photo Wall
```
NODE_ENV=15-photo_wall npm start
```
In this config you defined your first own photo wall entry (i.e. "memory"). When configuring own memories, they replace the original ones. This leaves some challenges impossible to solve, which is reported as validation errors in the config.

### 16. Default Challenge Memories
```
NODE_ENV=16-default_challenge_memories npm start
```
The quickest way to get back to a working configuration, is to add back all original memories from `default.yml` which were needed for hacking challenges. When starting the Juice Shop, you now see some of these plus your own original photo wall entry.

### 17. Avatars
```
NODE_ENV=17-avatars npm start
```
Launch any tutorial from the Score Board to see your overwritten Hacking Instructor avatar. Similarly, open the Support Chat Bot (when logged in) to enjoy its new avatar. 

### 18. Final Touch
```
NODE_ENV=18-final_touch npm start
```
This collection of smaller customizations are barely noticable. To check out all of their effect...
* ...visit the Accounts > Orders & Payments > Recycle page
* ...solve the _Blockchain Hype_ challenge
* ...and the _Exposed Metrics_ challenge.
