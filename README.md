 
# Authentication [POST]

These API endpoints require HTTP Token Authentication. The auth token must be
sent in the HTTP headers in the following form:

`
Authorization: Token {auth_token}
`
For example, if your auth token is `eeN3EiwuShowaih6ceic5ohchahvu4quaeg9eing1`,
you MUST send the header `Authorization: Token
eeN3EiwuShowaih6ceic5ohchahvu4quaeg9eing1` in all your requests to these 
endpoints.

To obtain a token, the API endpoint `POST /accounts/get_auth_token/` is provided.

# get_movie_details [POST]

- API end point is `POST /api/get_movie_details`
- Any user can view details, super user is not needed.
- request example is:
`{"movie_name":"m1"}`
OR
`{"director_name":"d1"}`
- response example:
`
{"movie_name":"m1",
"director_name":"d1",
"imdb_score":1.2,
"popularity":1.3,
 "genre":["Family"]
}`

# add_movie_details

- This API is used to add movie details.
- All fields are compulsory.
- Only superuser(admin) have access to this API.

request body example:
`
{"movie_name":"m1",
"director_name":"d1",
"imdb_score":1.2,
"popularity":1.3,
 "genre":["Family"]
}`
- on success response will be
`success`

# update_movie_details

- This API is used to edit movie details.
- All fields are compulsory.
- Only superuser(admin) have access to this API.

- request body example:
`
{"movie_name":"m1",
"director_name":"d1",
"imdb_score":1.2,
"popularity":1.3,
 "genre":["Family"]
}`
- on success response will be
`success`

# delete_movie_details
- This API is used to delete movie details.
- Delete is possible only with movie name
- Only superuser(admin) have access to this API.
- request body example:
- `{"movie_name":"m1"}`
- on success response will be
`success`

### NOTE:
- In case of error for any API, the reason of failure is returned.
