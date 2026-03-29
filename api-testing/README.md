# API Testing — Postman Diary

Structured API testing practice using the [Grocery Store API](https://simple-grocery-store-api.click).

## Topics Covered

| Day | Topic |
|-----|-------|
| Day 01–03 | Environment setup, `{{BaseURL}}`, GET /products, status code testing |
| Day 04–05 | Query params vs path params, POST /carts (201), GET /carts/{cartId} |
| Day 06–07 | Status code experiments (400/401/403/404), collection folder organization |
| Day 07+ | JavaScript fundamentals: `let`/`const`, if-else, arrays, for loops, functions |
| Days 08–10 | `pm.test` assertions, JSON assertions, environment variables *(in progress)* |

## JavaScript Assertions Used

```javascript
pm.test("Status code is 200", () => {
  pm.response.to.have.status(200);
});

pm.test("Response has products", () => {
  const json = pm.response.json();
  pm.expect(json).to.be.an('array');
  pm.expect(json.length).to.be.greaterThan(0);
});
```

## Notable Bug Found

**`GET /products?limit=3` returns 20 products instead of 3**

The `limit` query parameter is not implemented on this endpoint. Verified via:
```javascript
console.log(pm.response.json().length); // returns 20, not 3
```

This demonstrates: parameter validation testing, using Postman Console for debugging, and identifying backend defects during API testing.

## Screenshots

![Postman limit bug](https://raw.githubusercontent.com/anadanelia369/QA-Portfolio/main/assets/postman-limit-bug.png)
