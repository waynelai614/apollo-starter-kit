# apollo-starter-kit

Boilerplate for getting off the ground quickly when writing a GraphQL server.

See also [Tutorial: How to build a GraphQL server](https://medium.com/apollo-stack/tutorial-building-a-graphql-server-cddaa023c035#.wy5h1htxs) and the solution in the `server-tutorial-solution` branch of this repo.

## Getting started

```sh
git clone https://github.com/waynelai614/apollo-starter-kit.git
cd apollo-starter-kit
npm install
npm run start
```

Then open [http://localhost:8080/graphql](http://localhost:8080/graphql)

When you paste this on the left side of the page:

```
{
  author(firstName: "Edmond") {
    id
    firstName
    lastName
    posts {
      id
      title
      text
    }
  }
  getFortuneCookie
}
```

and hit the play button (cmd-return), then you should get this on the right side:

```json
{
  "data": {
    "author": {
      "id": 2,
      "firstName": "Edmond",
      "lastName": "Jones",
      "posts": [
        {
          "id": 2,
          "title": "A post by Edmond",
          "text": "Harum ullam pariatur quos est quod. Ea quisquam esse quia et commodi autem. Ut exercitationem maiores et voluptas."
        }
      ]
    },
    "getFortuneCookie": "sunt aut facere repellat provident occaecati excepturi optio reprehenderit"
  }
}
```  
