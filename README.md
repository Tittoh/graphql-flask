# Python Flask GraphQL with Graphene
Python-Flask and graphql app

#### Testing Environment

```
$ pip install virtualenv
$ virtualenv venv
$ source venv/bin/activate
```

#### Dependencies()
Install using `pip` inside the environment.

```
flask
flask-graphql
flask-migrate
flask-sqlalchemy
graphene
graphene-sqlalchemy
```

### Running the app.
Run `python seed.py` to initialize the database

`python app.py` to start the app.



## Rest API examples
`GET http://127.0.0.1:5000/`

## Graphql query-api example
### Fetch
```
POST http://127.0.0.1:5000/graphql-query
Content-Type: application/graphql
```

```
{
  allPosts{
    edges{
      node{
        title
        author{
          email
        }
      }
    }
  }
}
```

## Graphql mutation-api example
### Create new

```
POST http://127.0.0.1:5000/graphql-mutation
Content-Type: application/graphql
```
```
mutation {
  savePost(email:"tittohtech@gmail.com", title:"Title 2", body:"Blog post 2") {
    post{
      title
      body
      author{
        email
      }
    }
  }
}
```

**[Tittoh Tech](https://www.tittohtech.com)**

