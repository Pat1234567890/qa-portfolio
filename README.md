{
  "info": {
    "name": "Urban Lunch API Smoke Tests",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
  },
  "item": [
    {
      "name": "GET /dishes",
      "request": {
        "method": "GET",
        "header": [],
        "url": { "raw": "https://api.urbanlunch.local/v1/dishes", "host": ["https://api.urbanlunch.local"], "path": ["v1","dishes"] }
      },
      "response": [],
      "event": [
        {
          "listen": "test",
          "script": {
            "exec": [
              "pm.test('Status code is 200', () => pm.response.to.have.status(200));",
              "pm.test('Response contains dishes array', () => pm.response.json().hasOwnProperty('dishes'));"
            ]
          }
        }
      ]
    },
    {
      "name": "POST /orders",
      "request": {
        "method": "POST",
        "header": [{"key":"Content-Type","value":"application/json"}],
        "body": {
          "mode": "raw",
          "raw": "{\"dish_id\":1,\"pickup_point_id\":2}"
        },
        "url": { "raw": "https://api.urbanlunch.local/v1/orders", "host": ["https://api.urbanlunch.local"], "path": ["v1","orders"] }
      },
      "event": [
        {
          "listen": "test",
          "script": {
            "exec": [
              "pm.test('Order created (201)', () => pm.response.to.have.status(201));",
              "pm.test('Response has order_id', () => pm.response.json().hasOwnProperty('order_id'));"
            ]
          }
        }
      ]
    }
  ]
}


