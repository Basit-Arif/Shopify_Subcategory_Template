# Subcategory Slider

<img width="1437" alt="Screenshot 2024-07-09 at 4 21 41 PM" src="https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/ac3e369f-93cb-4314-9613-1a3c1b5af842">

## Overview

This custom carousel slider is designed for subcategories within the store, ensuring a consistent and visually appealing UI across all subcategories.

## Features

- Responsive Design: Adjusts seamlessly to different screen sizes.
- Hover Effects: Images scale up on hover for a dynamic effect.
- Flexible Item Display: Easily configurable to display 1 to 4 items per row.

# Usage Instructions

## Settings Configuration
1. #### Items per Row:
   - Navigate to the slider settings.
   - Adjust the Items per Row slider to set the number of items you want to display per row (1-4).
   
## Adding Items
1. #### Upload Images:
    - For each collection item, upload an image using the Image setting.

2. #### Set Titles and URLs:
    - Provide a title for each collection item using the Title setting.
    - Enter the URL where clicking the item will navigate using the Link URL setting.

## Customization
1. #### Stylesheet Adjustments:
    - Modify the dimensions, hover effects, and other styles in the stylesheet provided.
    - Adjust the maximum width, padding, and margin to fit your store's theme.

## Example Implementation

Schema Of Slider:
```st
{% schema %}
{
  "name": "Slider(toddler girl)",
  "settings": [
    {
      "type": "header",
      "content": "Slider Settings"
    },
    {
      "type": "range",
      "id": "items_per_row",
      "label": "Items per Row",
      "min": 1,
      "max": 4,
      "step": 1,
      "default": 4
    }
  ],
  "blocks": [
    {
      "type": "collection_item",
      "name": "Collection Item",
      "settings": [
        {
          "type": "image_picker",
          "id": "item_image",
          "label": "Image",
          "info": "Upload an image for this collection item."
        },
        {
          "type": "text",
          "id": "item_title",
          "label": "Title",
          "default": "Collection Item Title"
        },
        {
          "type": "url",
          "id": "item_url",
          "label": "Link URL",
          "info": "Enter the URL where clicking the item will navigate."
        }
      ]
    }
  ],
  "presets": [
    {
      "name": "Slide(toddler)",
      "category": "Custom",
      "blocks": [
        { "type": "collection_item" },
        { "type": "collection_item" },
        { "type": "collection_item" },
        { "type": "collection_item" }
      ]
    }
  ]
}
{% endschema %}
```
The above code is the schema for the slider, detailing its settings and block structure. It allows for easy customization and ensures a consistent look across different subcategories by providing settings for the number of items per row and the ability to add images, titles, and URLs for each collection item

## Subcategories

All subcategories have the same slider configuration to maintain a consistent user interface. Adjust the required_titles array in the Liquid code to match the subcategory names in your store.

## Step by Step Implementation with visuals
![1](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/33264cf4-d50e-4a7e-b621-e29acb5ccb5c)
![2](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/df2505d9-20d7-4a76-b471-5cc887941616)
![3](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/62a88e0e-9c73-4a8e-9fa5-f87c22ea395d)
![4](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/a1bd85b7-6bee-4a59-a2c1-6b6d557f7868)
![5](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/2b466db3-d931-47c6-b3fe-2289535de070)
![6](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/e0184073-efc2-4187-b17b-09e6f4069166)
![7](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/228b4d10-f1c4-4f8c-9c0f-74b54d4521a8)
![8](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/0968bfb2-2840-44d3-8083-53f3b78f4d38)
![9](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/32d0fdf0-0273-4084-adbe-2098e369c58d)
![10](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/63f97142-e0e3-4de8-bdbc-2d11564d1011)
![11](https://github.com/Basit-Arif/Shopify_Subcategory_Template/assets/26505810/02e85ee4-ffed-47ae-9250-91e9ff0bacd2)



