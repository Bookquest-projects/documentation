# documentation

## API

#### Login

<details>
 <summary><code>POST</code> <code><b>/login</b></code></summary>

##### Parameters

###### Body parameters

`email` *required* string

`password` *required* string

##### Responses

```json
{
  "access_token": "string"
}
```

</details>

------------------------------------------------------------------------------------------

#### Register

<details>
 <summary><code>POST</code> <code><b>/register</b></code></summary>

##### Parameters

###### Body parameters

`email` *required* string

`password` *required* string

##### Responses

```json
{
  "access_token": "string"
}
```

</details>

------------------------------------------------------------------------------------------

#### Books

<details>
 <summary><code>POST</code> <code><b>/books/scan</b></code></summary>

##### Parameters

###### Body parameters

`image` *required* string

##### Responses

```json
{
  "title": "string",
  "subtitle": "string",
  "publisher": "string",
  "published_date": "string",
  "description": "string",
  "authors": [
    "string"
  ],
  "page_count": number,
  "categories": [
    "string"
  ],
  "average_rating": number,
  "ratings_count": number,
  "isbn": "string",
  "image_link": "string",
  "language": "string"
}
```

</details>

<details>
 <summary><code>GET</code> <code><b>/books/{isbn}</b></code></summary>

##### Parameters

###### Path parameters

`isbn` *required* string

##### Responses

```json
{
  "title": "string",
  "subtitle": "string",
  "publisher": "string",
  "published_date": "string",
  "description": "string",
  "authors": [
    "string"
  ],
  "page_count": number,
  "categories": [
    "string"
  ],
  "average_rating": number,
  "ratings_count": number,
  "isbn": "string",
  "image_link": "string",
  "language": "string"
}
```

</details>

<details>
 <summary><code>GET</code> <code><b>/books/{isbn}/recommendations</b></code></summary>

##### Parameters

###### Path parameters

`isbn` *required* string

##### Responses

```json
[
  {
    "title": "string",
    "subtitle": "string",
    "publisher": "string",
    "published_date": "string",
    "description": "string",
    "authors": [
      "string"
    ],
    "page_count": number,
    "categories": [
      "string"
    ],
    "average_rating": number,
    "ratings_count": number,
    "isbn": "string",
    "image_link": "string",
    "language": "string"
  }
]
```

</details>

------------------------------------------------------------------------------------------

#### Authors

<details>
 <summary><code>GET</code> <code><b>/authors/{name}</b></code></summary>

##### Parameters

###### Path parameters

`name` *required* string

##### Responses

```json
{
  "name": "string",
  "books": [
    {
      "title": "string",
      "subtitle": "string",
      "publisher": "string",
      "published_date": "string",
      "description": "string",
      "authors": [
        "string"
      ],
      "page_count": number,
      "categories": [
        "string"
      ],
      "average_rating": number,
      "ratings_count": number,
      "isbn": "string",
      "image_link": "string",
      "language": "string"
    }
  ]
}
```

</details>






