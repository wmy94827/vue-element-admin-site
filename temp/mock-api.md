# Mock Data

Mock data is an integral part of the front-end development process, the key link to separate the front and back-end development. By pre-agreed interfaces with the server side, simulating request data or even logic enables front-end development to be independent and not blocked by server-side development.

## Swagger
In my company project, the data is usually simulated by the backend using [swagger](https://swagger.io/).
`swagger`it is a REST APIs document generation tool that can cross-platform automatically generated from code comments, open source, support most of the language, the community is good. In short, it is very good and strongly recommended.

[Online Demo](http://petstore.swagger.io/?_ga=2.222649619.983598878.1509960455-2044209180.1509960455#/pet/addPet)

## Easy-mock
[vueAdmin-template](https://github.com/PanJiaChen/vueAdmin-template) uses [easy-mock](https://easy-mock.com/login) to simulate the data.
It is a pure front-end visualization, and can quickly generate simulation data persistence services. It's very easy to use and can be combined with `swagger`. It's worth a try for both the team and the individual project.

[Online Demo](https://easy-mock.com/)

## Mockjs
[vue-element-admin](https://github.com/PanJiaChen/vue-element-admin) is a purely front-end personal project, so the data is generated by [mockjs](https://github.com/nuysoft/Mock). Its principle is: intercept all the requests and proxy to the local simulation data, so no request is issued in the network.

If you need to revamp this project, removing mockjs is easy.

All mock data is in the `src/mock` directory. It will only intercept the url you declared in `src/mock/index.js`.

**Remove: ** Just remove `import '/Mock'` from` src/main.js` and delete the `src/mock` folder.