# Secret Family Recipes API


Base URL: https://secret-family-recipes-1.herokuapp.com/

# Users

| Field Name | Data Constraints           |
| ---------- | -------------------------- |
| id         | integer, primary key, auto |
| username   | string, required           |
| password   | string, required, hashed   |

| Endpoint                | Purpose                   | Success Response             | Success Code |
| ---------------------   | ------------------------- | -----------------------      | ------------ |
| POST /api/auth/register | load a user's tasks       | User data, Token             | 201          |
| POST /api/auth/login    | User login                | "Welcome to our API", Token  | 200          |

# Recipes

| Endpoint                | Purpose                   | Success Response                     | Success Code |
| ---------------------   | ------------------------- | ------------------------------------ | ------------ |
| Get /api/recipes        | Geting a list of recipes  | List a recipes                       | 200          |
| Get /api/recipes/:id    | Getting recipe by ID      | Returns single recipe by ID          | 200          |
| Post /api/recipes       | Post new recipe           | Returns single recipe                | 200          |
| Put /api/recipes/:id    | Edit/Modify recipe        | success: 'recipe modified', id: id   | 200          |
| Delete /api/recipes/:id | Delete Recipe             | success: 'recipe deleted'            | 200          |

# Ingredients

| Endpoint                         | Purpose                       | Success Response                   | Success Code |
| ---------------------------------| ----------------------------- | -----------------------------------| ------------ |
| Get /api/ingredients             | Geting a list of ingredients  | List a ingredients                 | 200          |
| Get /api/ingredients/:id         | Getting ingredients by ID     | Returns single ingredients by ID   | 200          |
| Get /api/recipes/:id/ingredients | Getting ingredients recipe ID | Returns single ingredients by ID   | 200          |
| Post /api/ingredients            | Post new ingredients          | success: 'new ingredient created'  | 200          |
| Put /api/ingredients/:id         | Edit/Modify ingredient        | success: 'ingredient modified',    | 200          |
| Delete /api/ingredients/:id      | Delete ingredient             | success: 'recipe deleted'          | 200          |



# Categories

| Endpoint                             | Purpose                               | Success Response                   | Success Code |
| -------------------------------------|---------------------------------------| -----------------------------------| ------------ |
| Get /api/recipes/categories          | Returns a list if existing categories | List of existing categories        | 200          |
| Post /api/categories                 | Post new recipe category              | category created                   | 201          |
| Put /api/recipes/categories/:id      | Edit/Modify category                  | category edited                    | 200          |
| Delete /api/recipes/categories/:id   | Delete category                       | success: 'category deleted'        | 200          |


# Steps

| Endpoint                             | Purpose                               | Success Response     | Success Code |
| -------------------------------------| --------------------------------------| ---------------------| ------------ |
| Get /api/recipes/:id/steps           | Returns a list of steps for recipe    | List of steps        | 200          |
| Post /api/recipes/steps              | Post new recipe instruction           | list of steps        | 201          |

 


