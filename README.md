# Feature Extraction from Images

### Problem Statement

In this hackathon, the goal is to create a machine learning model that extracts entity values from images. This capability is crucial in fields like healthcare, e-commerce and content moderation, where precise information is vital. As digital marketplaces expand, many products lack detailed textual descriptions, making it essential to obtain key details directly from images. These images provide important information listed below - 

Feature names : Height, Width, Depth, Volume, Wattage, Voltage, Maximum_weight_recommendation, Item_weight

### Data Description
1. index - A unique identifier for the data sample
2. image_link - Public URL where the product image is available to download
3. group_id - Category code of the product
4. entity_name - Product entity name. Example - "Height"
5. entity_value - Product entity value. Example - "35 cm"

### Example of a Prediction

![prediction](https://github.com/user-attachments/assets/3fc42816-543b-43e9-8171-26bef9120b1c)

The entity_name provided for this image was "Height", i.e. the model should find the height of the product from the image

In this prediction, the image was first given to YOLO to distinguish between width and height in the image using Bounding Boxes. After getting the boxes, OCR was performed only on the "Height" bounding box, and the result was "1.9 in".
