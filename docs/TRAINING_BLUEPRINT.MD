# Training & Quality Standards: Recipe Catalogue Blueprint

## 1. Overview
**Owner:** Jake Morrison (Training and Quality Standards)
**Objective:** Centralize all recipes and standard operating procedures (SOPs) from disconnected Google Drive folders into a structured, easily searchable developer-friendly catalog. This foundation will eventually support automated translations (English/Spanish) and AI-powered quick search for kitchen staff.

---

## 2. Data Structure (Recipe Schema)
Every recipe or procedure in the catalog must adhere to the following JSON-compatible format to ensure future compatibility with databases and front-end UIs:

```json
{
  "id": "slug-string-lowercase",
  "title": "Recipe Name",
  "category": "Kitchen | Grill | Prep | Bar",
  "language": "en | es",
  "metadata": {
    "prep_time_mins": 15,
    "cook_time_mins": 10,
    "grill_temperature_f": 400
  },
  "ingredients": [
    {
      "name": "Ingredient Name",
      "quantity": 1.5,
      "unit": "lbs | oz | items | tbsp"
    }
  ],
  "instructions": [
    {
      "step": 1,
      "description": "Detailed text of step 1."
    }
  ]
}
