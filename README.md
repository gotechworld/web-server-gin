# The codebase includes the following sections

+ Design API endpoints.
+ Create a folder for your code.
+ Create the data.
+ Write a handler to return all items.
+ Write a handler to add a new item.
+ Write a handler to return a specific item.

## Writing a RESTful web service API with Go and the Gin Web Framework with two endpoints

__/albums__

_GET_ – Get a list of all albums, returned as JSON.
_POST_ – Add a new album from request data sent as JSON.

__/albums/:id__

_GET_ – Get an album by its ID, returning the album data as JSON. 

### From a different command line window, use __curl__ to make a request to your running web service

```
$ curl http://localhost:5000/albums \
    --include \
    --header "Content-Type: application/json" \
    --request "POST" \
    --data '{"id": "4","title": "The Modern Sound of Betty Carter","artist": "Betty Carter","price": 49.99}'
```

### Use __curl__ to retrieve the full list of albums, which you can use to confirm that the new album was added

```
$ curl http://localhost:5000/albums \
    --header "Content-Type: application/json" \
    --request "GET"
```


