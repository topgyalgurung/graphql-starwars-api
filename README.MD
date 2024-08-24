# GraphQL Exercise

-  retrieve and manipulate data with GraphQL from  Star Wars API (SWAPI)

## 1. basic tasks 
### 1. List all Films 
```
query Query {
    allFilms {
      films {
        title
      }
      }
  }
  ```
### 2. Fetch a specific character
```
{
  allPeople {
    people {
      id
      name
    }
  }
}
#### response
```
    {
    "data": {
        "allPeople": {
        "people": [
            {
            "id": "cGVvcGxlOjE=",
            "name": "Luke Skywalker"
            },
            {
            "id": "cGVvcGxlOjI=",
            "name": "C-3PO"
            },
            {
            "id": "cGVvcGxlOjM=",
            "name": "R2-D2"
            },
```
- pick one name you want to get using their unique id 
```
    {
        person(id: "cGVvcGxlOjE=") {
        name

    }
