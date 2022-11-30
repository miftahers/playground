## USERS
### REGISTER
Butuh data:
- email
- username
- password
```
POST /api/v1/users/register
```
### LOGIN
Butuh data:
- email
- password
```
POST /api/v1/users/login
```
## TOPICS
### CREATE
Butuh data:
- name
- description
```
POST /api/v1/topics/create
```
### EDIT DESCRIPTION
Butuh data:
- description
- topic_id (via URL Parameter)
```
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
### DELETE TOPIC
Butuh data:
- topic_id (via URL Parameter)
```
DELETE /api/v1/topics/delete/:topic_id
```
## POSTS
### CREATE
Butuh data:
- title
- photo (maintenance)
- body
- topic_name (via URL Parameter)
```
POST /api/v1/posts/create/:topic_name
```
### GET ALL POST
Butuh data:
- topic_name (via URL Parameter)
```
GET /api/v1/posts/all/:topic_name
```
### GET POST
Butuh data:
- post_id (via URL Parameter)
```
GET /api/v1/posts/:post_id
```
### EDIT POST
- title
- photo (maintenance)
- body
- post_id (via URL Parameter)
```
PUT /api/v1/posts/edit/:post_id
```
### DELETE POST
- post_id (via URL Parameter)
```
DELETE /api/v1/posts/delete/:post_id
```
## COMMENTS
### GET ALL COMMENT
Butuh data:
- post_id (via URL Parameter)
```
GET /api/v1/posts/comments/:post_id
```
### CREATE COMMENT
Butuh data:
- body
- post_id (via URL Parameter)
```
POST /api/v1/posts/comments/create/:post_id
```
### EDIT COMMENT
Butuh data:
- body
- comment_id (via URL Parameter)
```
PUT /api/v1/posts/comments/edit/:comment_id
```
### DELETE COMMENT
Butuh data:
- comment_id (via URL Parameter)
```
DELETE /api/v1/posts/comments/delete/:comment_id