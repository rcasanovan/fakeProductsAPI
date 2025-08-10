# Fake Products API

A fake REST API for testing and development purposes, powered by [my-json-server.typicode.com](https://my-json-server.typicode.com).

## How It Works

This repository uses [my-json-server.typicode.com](https://my-json-server.typicode.com) to instantly create a fake REST API from the `db.json` file. No server setup required!

### API Endpoints

Once the repository is pushed to GitHub, you can access the API at:

- **Base URL**: `https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI`
- **All Products**: `https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI/products`
- **Single Product**: `https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI/products/{id}`

### Available Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/products` | Get all products |
| GET | `/products/{id}` | Get a specific product by ID |
| GET | `/products?type={type}` | Filter products by type |

### Product Types

The API includes products in the following categories:
- **food**: Sandwiches, wraps, salads, pizza, etc.
- **drink**: Coffee, juice, soft drinks, energy drinks, etc.
- **dessert**: Chocolate bars, muffins, yogurt, cookies, etc.
- **snack**: Granola bars, peanuts, etc.
- **other**: Cheese & crackers, etc.

### Product Structure

Each product has the following properties:
```json
{
  "id": 1,
  "name": "Product Name",
  "image": "https://raw.githubusercontent.com/rcasanovan/fakeProductsAPI/main/Images/image.jpg",
  "price": 7.99,
  "inventory": 20,
  "type": "food"
}
```

## Usage Examples

### Get all products
```bash
curl https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI/products
```

### Get a specific product
```bash
curl https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI/products/1
```

### Filter by type
```bash
curl https://my-json-server.typicode.com/rcasanovan/fakeProductsAPI/products?type=drink
```

## About my-json-server.typicode.com

This service allows you to create instant fake REST APIs by simply:
1. Creating a GitHub repository
2. Adding a `db.json` file with your data
3. Accessing your API at `https://my-json-server.typicode.com/{username}/{repo}`

**Note**: Changes are faked and not persisted, requests are cached for 1 minute, and all servers are public.

## Repository Structure

```
fakeProductsAPI/
├── db.json          # Main data file with products
├── Images/          # Product images
└── README.md        # This file
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.