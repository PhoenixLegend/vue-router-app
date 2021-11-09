# vue-router-app

## Project setup

```
npm install
```

### Compiles and hot-reloads for development

```
npm run serve
```

### Compiles and minifies for production

```
npm run build
```

### Lints and fixes files

```
npm run lint
```

### Customize configuration

See [Configuration Reference](https://cli.vuejs.org/config/).

###notes###
<router> link will not refresh the page but the <a> link does
router for internal links a for others.

###lazy load###
look at the chrome network tag and select js.
you will see that the app.js was already loaded. no matter which page you navigate to,
this app.js will stay there. because all the js file were load the first time.
What if you can load each js file when the route is loaded, that is call lazy load, which
will make your app smooth and even faster.

magic comment to name each js file

    // route level code-splitting
    // this generates a separate chunk (about.[hash].js) for this route
    // which is lazy-loaded when the route is visited.
    component: () =>
      import(/* webpackChunkName: "about" */ "../views/About.vue"),

more info @ https://vueschool.io/lessons/dynamically-load-components

###$route###
open el:root in vue plugin, you will see the instance of all the elements including params is all there.

routerlinks will let us know path only by name.
