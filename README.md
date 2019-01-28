# Ey 🐭 How can i serve you?

The fastest, zero dependency, small express style node router.

Ey supports plain string, regex, and parameterized routes.
It also returns a simple (req, res) function to infinitely nest apps in your routing as you please.

Should be compatible with most express / connect packages like [`body-parser`](https://npmjs.org/package/body-parser), [`serve-static`](https://npmjs.org/package/serve-static) and [`finalhandler`](https://npmjs.org/package/finalhandler).

## Getting started

```js
const ey = require('ey')
    , http = require('http')

const app = ey()

app
  .get('/', (req, res) => res.end('Hello World.'))
  .get('/users', getUsers)
  .get('/users/:userId', getUsers)
  .delete('/users/:userId', deleteUser)
  .use(bodyParser.json())
  .post('/users', createUser)
  .put('/users/:userId', updateUser)

http.createServer(app).listen(3000)
```

## More documentation under way
