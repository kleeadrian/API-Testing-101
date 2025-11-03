# API-Testing-101

Exercise 1 
ENDPOINT - https://library-api.postmanlabs.com/books

```
_pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});_
```


```
_pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});_
```
Exercise 2
 ENDPOINT - https://library-api.postmanlabs.com/books
```
// 1. Check status code is 201
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

// 2. Assert response time < 1000ms
pm.test("Response time is less than 1000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(1000);
});

// 3. Validate response is JSON
pm.test("Response is JSON", function () {
    pm.response.to.be.json;
});

// 4. Save id as collection variable
pm.test("Save book id as collection variable", function () {
    var jsonData = pm.response.json();
    pm.collectionVariables.set("bookId", jsonData.id);
});
```

BODY of Request
```
{
  "title": "Harry Potter",
  "author": "JK Rowling",
  "genre": "fantasy",
  "yearPublished": 1997
}
```
Excercise 3 
ENDPOINT - https://library-api.postmanlabs.com/books/:id
```
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```
Exercise 4 -
ENDPOINT - https://library-api.postmanlabs.com/books/:id
```
// Test that the response status code is 200
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

// Test that the response time is less than 500ms
pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});

// Test that the response body is empty or null
pm.test("Response body is empty or null", function () {
    var body = pm.response.text();
    pm.expect(body === "" || body === null).to.be.true;
});
```
