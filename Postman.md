# Postman Configuration

### HTTP

**Request** (Address, Request Method, Headers, Body)

**Response** (Status Code, Headers, Body)

**HTTP Request Methods:** Most Common 
1. GET: Retrieve some data
2. POST: Submit JSON

### JSON

Why do we use JSON?
- JSON has a simple key value format, similar to dictionary.
- The complete enclosed curly braces `{ }` is called as an object.
```json
{
    "Key Name": "Value"
}
```

Example:
```json
{
    "firstName": "Kirankumar",
    "age": 28,
    "isMale": true,
    "isMarried": false,
    "hobbies": ["Walking", "Reading", "Travelling"]
}
```
- We use JSON to transfer data, two systems use JSON to share the data and communicate with each others.
- Suppose both the systems are using different programming language, so they will transfer th data in JSON format.
- The other system will receive the data and parse the JSON and will transform into known language.
