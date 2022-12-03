## USERS
`REGISTER`
```
Butuh data:
- email
- username
- password

POST /api/v1/users/register
```
`LOGIN`
```
Butuh data:
- email
- password

POST /api/v1/users/login
```
### GET USERS
```
Butuh data:
- page (via Query Parameter)

GET /api/v1/users?page=
```
## TOPICS 
### CREATE {JWT}
```
Butuh data:
- name
- description

POST /api/v1/topics/create
```
### EDIT DESCRIPTION {JWT}
```
Butuh data:
- description
- topic_id (via URL Parameter)

PUT /api/v1/topics/edit_description/:topic_id
```
### GET ALL TOPICS
Butuh data:
- tidak ada
```
GET /api/v1/topics/
```
### GET TOPIC BY TOPIC_ID
Butuh data:
- topic_id (via URL Parameter)
```
GET /api/v1/topics/:topic_id
```
### DELETE TOPIC {JWT}
Butuh data:
- topic_id (via URL Parameter)
```
DELETE /api/v1/topics/delete/:topic_id
```
## POSTS
```
### CREATE {JWT}
Butuh data:
- title
- photo (maintenance)
- body
- topic_name (via URL Parameter)

POST /api/v1/posts/create/:topic_name

### GET ALL POST BY TOPIC_NAME
Butuh data:
- topic_name (via URL Parameter)
- page number (via Query Parameter)
*20 data per page

GET /api/v1/posts/all/:topic_name?page=

### GET POST by POST_ID
Butuh data:
- post_id (via URL Parameter)

GET /api/v1/posts/:post_id

### GET RECENT POST (ALL ENGGAK PER TOPIC LIMIT 20 Data)
Butuh data:
- page (via Query Parameter)
*20 data per page

GET /api/v1/posts/recent?page=

### EDIT POST {JWT}
- title
- photo (maintenance)
- body
- post_id (via URL Parameter)

PUT /api/v1/posts/edit/:post_id

### DELETE POST {JWT}
- post_id (via URL Parameter)

DELETE /api/v1/posts/delete/:post_id
```
## COMMENTS
```
### GET ALL COMMENT IN A POST BY POST_ID
Butuh data:
- post_id (via URL Parameter)

GET /api/v1/posts/comments/:post_id

### CREATE COMMENT {JWT}
Butuh data:
- body
- post_id (via URL Parameter)

POST /api/v1/posts/comments/create/:post_id

### EDIT COMMENT {JWT}
Butuh data:
- body
- comment_id (via URL Parameter)

PUT /api/v1/posts/comments/edit/:comment_id

### DELETE COMMENT {JWT}
Butuh data:
- comment_id (via URL Parameter)

DELETE /api/v1/posts/comments/delete/:comment_id
```
## REPLIES
```
### GET REPLIES BY COMMENT_ID
Butuh data:
- comment_id (via URL Parameter)

GET /api/v1/posts/comments/replies/:comment_id

### NEW REPLY {JWT}
Butuh data:
- body
- comment_id (via URL Parameter)

POST /api/v1/posts/comments/replies/create/:comment_id

### EDIT REPLY {JWT}
Butuh data:
- body
- comment_id (via URL Parameter)

PUT /api/v1/posts/comments/replies/edit/:comment_id

### DELETE REPLY {JWT}
- comment_id (via URL Parameter)

DELETE /api/v1/posts/comments/replies/delete/:comment_id
```
## LIKES
```
### LIKE {JWT}
Butuh data:
- post_id (via URL Parameter)

POST /api/v1/posts/likes/:post_id

### DISLIKE {JWT}

Butuh data:
- post_id (via URL Parameter)

POST /api/v1/posts/dislike/:post_id
```
