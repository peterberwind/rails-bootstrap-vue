# Rails 5.1 + BootstrapVue

https://bootstrap-vue.github.io/

```
$ rails new rails-bootstrap-vue --webpack=vue
$ cd rails-bootstrap-vue
$ yarn add bootstrap-vue
$ rails g controller Demo index
```

- Routing
 - config/routes.rb (root to: 'demo#index')
- HTML
 - app/views/layout/application.html.erb
 - app/views/demo/index.html.erb
- Vue.js
 - app/javascript/packs/demo.js
- webpack
 - config/webpack/shared.js

```
...
  resolve: {
    extensions: settings.extensions,
    modules: [
      resolve(settings.source_path),
      'node_modules'
    ],
    alias: {
	vue: 'vue/dist/vue.common.js'
    }
  },
...
```

```
$ bin/webpack
$ rails s
```
