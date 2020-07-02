# product-brief

## Project setup
```
yarn install
```

### Compiles and hot-reloads for development
```
yarn serve
```

### Compiles and minifies for production
```
yarn build
```

### Lints and fixes files
```
yarn lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### 关于Vue3框架CSS mobile样式自动继承桌面端样式的问题：
默认CSS下，桌面端和移动端CSS样式是完全分开的。这一点由 CSS中的 @media 很好的控制。
但是令人不喜欢的一点就是：Vue框架中在模板中写样式，@media 中的样式自动继承了桌面端的样式。
而非重新定义 @media 中的样式。这就造成了调 mobile样式的时候，会遇到各种奇怪的CSS bug。
只有通过浏览器审查才可以发现CSS问题出现在哪了。mobile中如果需要去掉某个样式，竟然还需要手写覆盖，
有时候还需要加 !important 才能覆盖成功。