# ERD05 - Cinema

## Entities

- Customer
- Receipt
- Receipt-Position
- Product
- Cook
- Recipe
- Ingredient
- Employee
- Waiter

## Attributes

### Product
- name
- recipe-id
- price
- ready-made

### Recipe
- id
- preparation-time
- product-name

### Ingredient
- id
- origin
- ingredientType-id
- price

### IngredientType
- id
- name

### RecipeIngredientTypeAssignment
- ingredientType-id
- recipe-id
- count

### Receipt
- id
- total
- (cashing Waiter) employee-id
- Customer-id

### ReceiptPosition
- position
- Product-name
- quantity
- Receipt-id
- Employee-id

### Cook
- Employee-id
- awardedstars

### CookProductAssignment
- Employee-id
- Product-id

### Waiter
- Employee-id
- servingspeed

### Employee
- id
- name

### Customer
- id

## 1. ERD in Martin/Crow’s Foot notation

![](/Users/quirin/Documents/3AHITM/Informationssysteme/Uebungen/ERD05/ERD05.png)

## 2. Relations

- Customer=(**_id_**, name)
- Recipe=(`RecipeID`, `ProductName`)
- IngredientType=(**_IngredientTypeID_**, name)
- Ingredient=(origin, price, `IngredientTypeID`)
- Product=(ready-made, price, **_name_**, `recipeID`)
- ReceiptPosition=(position, `receiptID`, `productname`, quantity, `employeeID`)
- Receipt=(**_receiptID_**, `employeeID`, `customerID`, total)
- Waiter=(servingspeed, `employeeID`)
- Employee=(name, **_employeeID_**)
- Cook(awardedStars, `employeeID`)
- IngredientTypeRecipeAssignments=(`recipeID`, `ingredientTypeID`)

## Notation
`foreign key`
**_primary key_**
