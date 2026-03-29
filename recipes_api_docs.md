# Recipes App API Docs

---

## 🔌 Routes

### Dish

#### GET /dishes
Returns all dishes

#### GET /dishes/:dishId
Returns a single dish

#### POST /dishes
Creates a new dish

#### PUT /dishes/:dishId
Updates a dish

#### DELETE /dishes/:dishId
Deletes a dish

---

## 🧩 JSON Structures

### Dish Object (Response Example)

```json
{
  "id": 1,
  "name": "Pasta",
  "category": "Dinner",
  "ingredients": [
    {
      "name": "Salt",
      "quantity": 1,
      "unit": "tsp"
    },
    {
      "name": "Garlic",
      "quantity": 2,
      "unit": "cloves"
    }
  ],
  "tools": [
    {
      "name": "Pot"
    },
    {
      "name": "Pan"
    }
  ],
  "instructions": [
    {
      "step_number": 1,
      "text": "Boil water"
    },
    {
      "step_number": 2,
      "text": "Add pasta"
    }
  ],
  "created_at": "2026-01-01",
  "updated_at": "2026-01-02"
}
```

---

### POST /dishes (Request Body)

```json
{
  "name": "Pasta",
  "category": "Dinner",
  "ingredients": [
    {
      "name": "Salt",
      "quantity": 1,
      "unit": "tsp"
    }
  ],
  "tools": [
    {
      "name": "Pot"
    }
  ],
  "instructions": [
    {
      "step_number": 1,
      "text": "Boil water"
    }
  ]
}
```

---

### POST /dishes (Response)

```json
{
  "message": "Dish created successfully",
  "dish": {
    "id": 1,
    "name": "Pasta",
    "category": "Dinner",
    "ingredients": [
      {
        "name": "Salt",
        "quantity": 1,
        "unit": "tsp"
      }
    ],
    "tools": [
      {
        "name": "Pot"
      }
    ],
    "instructions": [
      {
        "step_number": 1,
        "text": "Boil water"
      }
    ],
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

---

### PUT /dishes/:dishId (Request Body)

```json
{
  "name": "Updated Pasta",
  "category": "Dinner",
  "ingredients": [
    {
      "name": "Salt",
      "quantity": 2,
      "unit": "tsp"
    }
  ],
  "tools": [
    {
      "name": "Pot"
    }
  ],
  "instructions": [
    {
      "step_number": 1,
      "text": "Boil water"
    },
    {
      "step_number": 2,
      "text": "Add pasta"
    }
  ]
}
```

---

### PUT /dishes/:dishId (Response)

```json
{
  "message": "Dish updated successfully",
  "dish": {
    "id": 1,
    "name": "Updated Pasta",
    "category": "Dinner",
    "ingredients": [
      {
        "name": "Salt",
        "quantity": 2,
        "unit": "tsp"
      }
    ],
    "tools": [
      {
        "name": "Pot"
      }
    ],
    "instructions": [
      {
        "step_number": 1,
        "text": "Boil water"
      },
      {
        "step_number": 2,
        "text": "Add pasta"
      }
    ],
    "created_at": "2026-01-01",
    "updated_at": "2026-01-02"
  }
}
```

---

### DELETE /dishes/:dishId

```json
{
  "status": 200,
  "message": "Dish deleted successfully"
}
```
