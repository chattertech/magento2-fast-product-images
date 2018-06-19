# magento2-fast-product-images
Magento 2 fast product images, removes loading image from product images.

The deafult Magento 2 behavior for product images is to load a spinner, then load all the images in the fotorama gallery. This resulst in the sinner being up until the dom loads and js can take over and replace it. It makes even the fastest Magento 2 site seem slow. 

This module is quite simple in that it replaces the spinner with the first image in the gallery. So now the page should simply show the image and not make you feel like you are waiting for it to load.

# Installation
```
composer config repositories.magento2-fast-product-images git git@github.com:xumulus/magento2-fast-product-images.git
composer require xumulus/magento2-fast-product-images:dev-master -n
bin/magento module:enable Xumulus_FastGalleryLoad
bin/magento setup:upgrade
bin/magento setup:static-content:deploy
```
# Usage

Once installed the module should alter the image loading.  

There are no admin settings, the module can be disable if you would like to return to the default behavior.

