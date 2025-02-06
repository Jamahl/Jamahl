# Costco Shopware POC Content Deletion Process

This document outlines the process of identifying and deleting all existing content in the Costco Shopware instance. The goal was to ensure a clean slate for further customization and development.

## Content Identification

### Categories
- Retrieved all categories from the Shopware instance.
- **Categories Identified**:
  - Catalogue #1 (ID: 01938c22fc1b70f6b3dc798973f9eee1)
  - Food (ID: 77b959cf66de4c1590c7f9b7da3982f3)
  - Bakery products (ID: 19ca405790ff4f07aac8c599d4317868)
  - Fish (ID: 48f97f432fd041388b2630184139cf0e)
  - Sweets (ID: bb22b05bff9140f3808b1cff975b75eb)
  - Clothing (ID: a515ae260223466f8e37471d279e6406)
  - Women (ID: 8de9b484c54f441c894774e5f57e485c)
  - Men (ID: 2185182cbbd4462ea844abeb2a438b33)
  - Free time & electronics (ID: 251448b91bc742de85643f5fccd89051)

### Media Folders
- Retrieved IDs for media folders:
  - Product Media (ID: 01938c22fce77355984343a2e42dc98a)
  - Theme Media (ID: 01938c23038e72bd8e3c59bfa68fe68e)

### Media Files
- Retrieved all media files in the 'Product Media' folder:
  - shirt_600x600 (ID: 102ac62ba27347a688030a05c1790db7)
  - handschuh_600x600 (ID: 2de02991cd0548a4ac6cc35cb11773a0)
  - hemd_600x600 (ID: 5808d194947f415495d9782d8fdc92ae)
  - schokolade_600x600 (ID: 6968ad64888844679918c638e449ffc5)
  - shirt_blue_600x600 (ID: 6cbbdc03b43f4207be80b5f752d5a1c4)
  - mobile_600x600 (ID: 70e352200b5c45098dc65a5b47094a2a)
  - waschmaschine_600x600 (ID: 84356a71233d4b3e9f417dcc8850c82f)
  - shirt_red_600x600 (ID: f69ab8ae42d04e17b2bab5ec2ff0a93c)

### Products
- Retrieved all products:
  - Main product with advanced prices (ID: 11dc680240b04f469ccba354cbf0b967)
  - Main product with reviews (ID: 1901dc5e888f4b1ea4168c2c5f005540)
  - Main product (ID: 2a88d9b59d474c7e869d8071649be43c)
  - Main product, free shipping with highlighting (ID: 3ac014f329884b57a2cce5a29f34779c)
  - Variant product (ID: 43a23e0c03bf4ceabc6055a2185faa87)
  - Main product with properties (ID: c7bca22753c84d08b6178a50052b4146)

### Product Manufacturers
- Retrieved all product manufacturers:
  - shopware AG (ID: 01938c22fcae7286af7c8e320076445c)
  - Shopware Food (ID: 2326d67406134c88bcf80e52d9d2ecb7)
  - Shopware Fashion (ID: 7f24e96676e944b0a0addc20d56728cb)
  - Shopware Freetime (ID: cc1c20c365d34cfb88bfab3c3e81d350)

### Property Groups
- Retrieved all property groups:
  - Target group (ID: 1857bb30fe6448c88f8ad331cf6dfa0c)
  - Colour (ID: 269c7e40a54a462e884edb004c5f7bc8)
  - Ingredients (ID: 448f3d72803f4ac8afc0c1108739ddf4)
  - Size (ID: 75f353b589d04bf48e8a9ab1f5422b0e)
  - Material (ID: a67cdd9627cb488bb4cd91f3e8d66e32)

## Content Deletion

### Media Files
- Deleted all media files in the 'Product Media' folder.

### Categories
- Deleted all categories except 'Catalogue #1'.

### Products
- Deleted all products.

### Product Manufacturers
- Deleted all product manufacturers.

### Property Groups
- Deleted all property groups.

## Conclusion

The content deletion process was successfully completed, ensuring a clean slate for further development and customization of the Shopware instance for Costco.
