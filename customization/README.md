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
### 6. Emails
### 7. Favicon
### 8. Notifications off
### 9. Schema validation
### 10. First product
### 11. Default challenge products
### 12. Product Tampering Challenge
### 13. Christmas Special Challenge
### 14. More Products w/ reviews
### 15. Photo Wall
### 16. Default Challenge Memories
### 17. Avatars
### 18. Final Touch
