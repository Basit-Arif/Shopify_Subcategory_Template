# Subcategory Slider



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






