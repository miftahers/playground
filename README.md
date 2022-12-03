# USERS
`REGISTER`


Input:
- email
- username
- password
```
POST /api/v1/users/register
```
`LOGIN`


Input:
- email
- password
```
POST /api/v1/users/login
```
`GET USERS`


Input:
- page (QUERY)
```
GET /api/v1/users?page=
```
# TOPICS 
`CREATE {JWT}`


Input:
- name
- description
```
POST /api/v1/topics/create
```
`EDIT DESCRIPTION {JWT}`


Input:
- description
- topic_id (PATH)
```
PUT /api/v1/topics/edit_description/:topic_id
```
`GET ALL TOPICS`


Input:
- tidak ada
```
GET /api/v1/topics/
```
`GET TOPIC BY TOPIC_ID`


Input:
- topic_id (PATH)
```
GET /api/v1/topics/:topic_id
```
`DELETE TOPIC {JWT}`


Input:
- topic_id (PATH)
```
DELETE /api/v1/topics/delete/:topic_id
```
# POSTS
`CREATE {JWT}`


Input:
- title
- photo (maintenance)
- body
- topic_name (PATH)
```
POST /api/v1/posts/create/:topic_name
```
`GET ALL POST BY TOPIC_NAME`


Input:
- topic_name (PATH)
- page number (QUERY)
*20 data per page
```
GET /api/v1/posts/all/:topic_name?page=
```
`GET POST by POST_ID`


Input:
- post_id (PATH)
```
GET /api/v1/posts/:post_id
```
`GET RECENT POST (ALL ENGGAK PER TOPIC LIMIT 20 Data)`


Input:
- page (QUERY)
<i>*20 data per page</i>
```
GET /api/v1/posts/recent?page=
```
`EDIT POST BY POST_ID{JWT}`


Input:
- title
- photo (maintenance)
- body
- post_id (PATH)
```
PUT /api/v1/posts/edit/:post_id
```
`DELETE POST {JWT}`


Input:
- post_id (PATH)
```
DELETE /api/v1/posts/delete/:post_id
```
# COMMENTS
`GET ALL COMMENT IN A POST BY POST_ID`


Input:
- post_id (PATH)
```
GET /api/v1/posts/comments/:post_id
```
`CREATE COMMENT {JWT}`


Input:
- body
- post_id (PATH)
```
POST /api/v1/posts/comments/create/:post_id
```
`EDIT COMMENT {JWT}`


Input:
- body
- comment_id (PATH)
```
PUT /api/v1/posts/comments/edit/:comment_id
```
`DELETE COMMENT {JWT}`


Input:
- comment_id (PATH)
```
DELETE /api/v1/posts/comments/delete/:comment_id
```
# REPLIES
`GET REPLIES BY COMMENT_ID`


Input:
- comment_id (PATH)
```
GET /api/v1/posts/comments/replies/:comment_id
```
`NEW REPLY {JWT}`


Input:
- body
- comment_id (PATH)
```
POST /api/v1/posts/comments/replies/create/:comment_id
```
`EDIT REPLY {JWT}`


Input:
- body
- comment_id (PATH)
```
PUT /api/v1/posts/comments/replies/edit/:comment_id
```
`DELETE REPLY {JWT}`


Input:
- comment_id (PATH)
```
DELETE /api/v1/posts/comments/replies/delete/:comment_id
```
## LIKES

`LIKE {JWT}`


Input:
- post_id (PATH)
```
POST /api/v1/posts/likes/:post_id
```
`DISLIKE {JWT}`



Input:
- post_id (PATH)
```
POST /api/v1/posts/dislike/:post_id
```

# BOOKMARKS
`Add new Bookmark {JWT}`


Input:
- post_id (PATH)
```
POST /api/v1/posts/bookmarks/:post_id
```
`Delete Bookmark {JWT}`


Input:
- post_id (PATH)
```
DELETE /api/v1/posts/bookmarks/:post_id
```
`Get All Owned Bookmarks {JWT}`


Input:
- tidak ada
```
GET /api/v1/posts/bookmarks/all
```
