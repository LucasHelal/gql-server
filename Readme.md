# Tutorial GraphQL + Nome
[Creating A GraphQL Server With Node.js And Express](https://medium.com/codingthesmartway-com-blog/creating-a-graphql-server-with-node-js-and-express-f6dddc5320e1)

### Server 

```javascript
{
    message
}
```

### Server 2



```javascript
query getSingleCourse($courseID: Int!) {
    course(id: $courseID) {
        title
        author
        description
        topic
        url
    }
}
```

* Query Variables

```javascript
{ 
    "courseID":1
}
```

```javascript
mutation updateCourseTopic($id: Int!, $topic: String!) {
  updateCourseTopic(id: $id, topic: $topic) {
    ... courseFields
  }
}

fragment courseFields on Course {
  title
  author
  description
  topic
  url
}
```

* Query Variables

```javascript
{
  "id": 1,
  "topic": "JavaScript"
}
```