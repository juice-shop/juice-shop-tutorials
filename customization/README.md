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

### 9. Schema validation
```
NODE_ENV=09-schema_fixed npm start
```

### 10. First product
```
NODE_ENV=10-single_product npm start
```

### 11. Default challenge products
```
NODE_ENV=11-default_challenge_products npm start
```

### 12. Product Tampering Challenge
```
NODE_ENV=12-product_tampering_challenge npm start
```

### 13. Christmas Special Challenge
```
NODE_ENV=13-christmas_special_challenge npm start
```

### 14. More Products w/ reviews
```
NODE_ENV=14-more_products_with_reviews npm start
```

### 15. Photo Wall
```
NODE_ENV=15-photo_wall npm start
```

### 16. Default Challenge Memories
```
NODE_ENV=16-default_challenge_memories npm start
```

### 17. Avatars
```
NODE_ENV=17-avatars npm start
```

### 18. Final Touch
```
NODE_ENV=18-final_touch npm start
```
