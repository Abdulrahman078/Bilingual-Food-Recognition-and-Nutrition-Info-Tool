# Bilingual Food Recognition and Nutrition Information Tool

## Project Overview
This project demonstrates an AI-powered food recognition tool using images as input and provides detailed nutritional information. The tool supports both English and Arabic languages, allowing users to upload an image of food or a drink, and receive nutritional information in their selected language.

## Expected Outputs
- The tool outputs a detailed nutritional breakdown, including:
  - Food item
  - Serving size (in grams or milliliters, depending on the food type)
  - Calories
  - Macronutrients: Protein, Carbohydrates, Fats
  - Additional nutritional info: Sugars, Fiber, Sodium
- The nutritional information is displayed in either **English** or **Arabic**, based on user selection. 

## Tools and Models Used
1. **Visual Question Answering (VQA) Model:**
   - This model is specifically designed for visual question-answering tasks, making it suitable for extracting relevant information from images.

2. **Translation Model:**
   - Used to translate the food item name from English to Arabic.

3. **Nutritionix API:**
   - This API provides detailed nutritional data for various food items, including macronutrient values, calories, sugars, fiber, and serving sizes.

4. **Gradio:**
   - An easy-to-use tool that provides a user-friendly interface.

## Pipeline Explanation
1. **Food Recognition:** The `Salesforce/blip-vqa-base` model processes the uploaded image and identifies the food item by answering the question: "What is the food or the drink in the image?".

2. **Translation:** the `marefa-nlp/marefa-mt-en-ar` model translates the food item to provide the output in Arabic.

## Justification for Model and Pipeline Choices
1. **VQA Model - `Salesforce/blip-vqa-base`:** Selected for its ability to accurately interpret and identify objects in images, particularly food items. It allows flexible question-based recognition, which is essential for this tool's purpose.

2. **Translation Model - `marefa-nlp/marefa-mt-en-ar`:** Chosen for its effectiveness in translating individual words and short phrases, making it a better choice for translating food names compared to models like `Helsinki-NLP`, which are more suited for full sentences.


## Special Measures for Arabic Language Support
- **Formatting:** The nutritional information output in Arabic is formatted using HTML to support right-to-left text alignment, providing a better user experience.

## Usage Instructions
1. Run the application and upload an image of food or a drink.
2. Select your preferred language (English or Arabic) from the dropdown menu.
3. The tool will recognize the food item and fetch the nutritional information.
4. View the detailed nutritional information in the chosen language, including serving size, calories, macronutrients, sugars, fiber, and sodium.

## Links to Hugging Face Models
- **Visual Question Answering Model:** [Salesforce/blip-vqa-base](https://huggingface.co/Salesforce/blip-vqa-base)
- **Translation Model:** [marefa-nlp/marefa-mt-en-ar](https://huggingface.co/marefa-nlp/marefa-mt-en-ar)

## Example Images
- Predefined example images are provided for quick testing directly within the interface.

## Project Resources
- **Presentation Slides:** A presentation detailing the project's goals, workflow, models, and outputs is included in the repository.
- **Video Walkthrough:** A short video walkthrough of the project is also uploaded to the repository.

## Hugging Face Space
The project is also available on Hugging Face Space. Explore the project using the link below:

- [Bilingual Food Recognition and Nutrition Info Tool on Hugging Face](https://huggingface.co/spaces/Abduuu/Bilingual_Food_Recognition_and_Nutrition_Info_Tool)

## Video Walkthrough
A video walkthrough the project code and how it works:

- [Video Walkthrough](https://youtu.be/hox0dtcjm1A)

