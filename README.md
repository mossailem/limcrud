# LimCRUD
LimCRUD is library for create simple CRUD request for my project. This is use default fetch API from javascript.

# Initialize
First, add to your page.

```HTML
<script src="link-to-this-directory/limcrud.js" />
```
Change ```link-to-this-directory``` to your own directory.

Then, initialize when page onload.

```Javascript
window.onload = () => {
  const crud = new LimCRUD("auth-string");
}
```

Change ```auth-string``` with your own bearer string when needed. You have to include the "Bearer" string, e.g. "Bearer 98e2y938hd9f948f4f43".

Done! You're ready to go!

# Usage
You can perform some create, read, update, and delete (CRUD) operation with REST API. Here's list of them.
1. Create with create() and createPlain().
2. Read with read().
3. Update with update() and updatePatch().
4. Delete with update().

Here's some example that frequently I used.

## Create
```Javascript
crud.create({
  url: "http://localhost/yourweb/api/user",
  data: {
    "name": "Sujono",
    "age": 20
  },
  name: "user"
});
```

## Read
```Javascript
crud.read({
  url: "http://localhost/yourweb/api/user/1"
});
```

## Update - Patch
```Javascript
crud.updatePatch({
  url: "http://localhost/yourweb/api/user/1",
  data: {
    "column": "age",
    "value": 20
  },
  name: "user"
});
```

## Delete
```Javascript
crud.delete({
  url: "http://localhost/yourweb/api/user/1"
});
```
