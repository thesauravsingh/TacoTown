# Taco Town 🌮

## Overview
Taco Town is a simple Express.js application that displays taco recipes based on the user's choice of protein. Users can select from Chicken, Beef, or Fish tacos, and the corresponding recipe details will be displayed.

## Features
- Displays a list of taco recipes with their ingredients and preparation details.
- Users can select a protein to view the associated taco recipe.
- Simple and clean user interface.

## Setup and Installation
To run this project locally, follow these steps:

### Prerequisites
- Node.js (v12 or higher)
- npm (Node Package Manager)

### Installation
1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/taco-town.git
    cd taco-town
    ```

2. **Install the dependencies:**
    ```bash
    npm install
    ```

3. **Run the application:**
    ```bash
    npm start
    ```

    The application will start on `http://localhost:3000`.

## Usage
1. Open your web browser and navigate to `http://localhost:3000`.
2. Select your favorite taco ingredient by clicking on one of the buttons (Chicken, Beef, or Fish).
3. The recipe for the selected taco will be displayed.

## Project Structure
```bash
.
├── public
│   ├── styles
│   │   └── main.css         # CSS file for styling
├── views
│   └── index.ejs            # EJS template for rendering the HTML
├── package.json             # Project dependencies and scripts
├── README.md                # Project overview and setup instructions
└── index.js                 # Main server file
```

## Code Explanation

### `index.js`
This is the main server file where the Express server is set up. It contains the following key sections:
- **Importing modules**: Import `express` and `body-parser`.
- **Recipe data**: The JSON data for the recipes is hardcoded into the file.
- **Middleware setup**: Set up `express.static` to serve static files and `body-parser` to parse form data.
- **Routes**:
  - `GET /`: Renders the main page with the recipe data.
  - `POST /recipe`: Handles the form submission to filter and display the recipe based on the selected protein.

### `views/index.ejs`
This is the EJS template that renders the HTML for the application. It displays the form for selecting a protein and dynamically shows the selected recipe details.

## Example JSON Data
```json
[
  {
    "id": "0001",
    "type": "taco",
    "name": "Chicken Taco",
    "price": 2.99,
    "ingredients": {
      "protein": {
        "name": "Chicken",
        "preparation": "Grilled"
      },
      "salsa": {
        "name": "Tomato Salsa",
        "spiciness": "Medium"
      },
      "toppings": [
        {
          "name": "Lettuce",
          "quantity": "1 cup",
          "ingredients": ["Iceberg Lettuce"]
        },
        {
          "name": "Cheese",
          "quantity": "1/2 cup",
          "ingredients": ["Cheddar Cheese", "Monterey Jack Cheese"]
        },
        {
          "name": "Guacamole",
          "quantity": "2 tablespoons",
          "ingredients": ["Avocado", "Lime Juice", "Salt", "Onion", "Cilantro"]
        },
        {
          "name": "Sour Cream",
          "quantity": "2 tablespoons",
          "ingredients": ["Sour Cream"]
        }
      ]
    }
  },
  {
    "id": "0002",
    "type": "taco",
    "name": "Beef Taco",
    "price": 3.49,
    "ingredients": {
      "protein": {
        "name": "Beef",
        "preparation": "Seasoned and Grilled"
      },
      "salsa": {
        "name": "Salsa Verde",
        "spiciness": "Hot"
      },
      "toppings": [
        {
          "name": "Onions",
          "quantity": "1/4 cup",
          "ingredients": ["White Onion", "Red Onion"]
        },
        {
          "name": "Cilantro",
          "quantity": "2 tablespoons",
          "ingredients": ["Fresh Cilantro"]
        },
        {
          "name": "Queso Fresco",
          "quantity": "1/4 cup",
          "ingredients": ["Queso Fresco"]
        }
      ]
    }
  },
  {
    "id": "0003",
    "type": "taco",
    "name": "Fish Taco",
    "price": 4.99,
    "ingredients": {
      "protein": {
        "name": "Fish",
        "preparation": "Battered and Fried"
      },
      "salsa": {
        "name": "Chipotle Mayo",
        "spiciness": "Mild"
      },
      "toppings": [
        {
          "name": "Cabbage Slaw",
          "quantity": "1 cup",
          "ingredients": [
            "Shredded Cabbage",
            "Carrot",
            "Mayonnaise",
            "Lime Juice",
            "Salt"
          ]
        },
        {
          "name": "Pico de Gallo",
          "quantity": "1/2 cup",
          "ingredients": ["Tomato", "Onion", "Cilantro", "Lime Juice", "Salt"]
        },
        {
          "name": "Lime Crema",
          "quantity": "2 tablespoons",
          "ingredients": ["Sour Cream", "Lime Juice", "Salt"]
        }
      ]
    }
  }
]
```

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue to discuss improvements or report bugs.

## License
This project is licensed under the MIT License.

---

This README file provides a comprehensive overview of the Taco Town project, including setup instructions, usage, project structure, and code explanations.
