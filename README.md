# support-ie8


## polyfill

在页面引入 polyfil

```html
<!-- Polyfills -->

    <!-- console-polyfill es5-shim es5-shim/es5-sham es6-shim es6-shim/es6-sham html5shiv media-match -->
    <!--[if lt IE 10]>
    <script src="/polyfill-lt-ie10.js"></script>
    <![endif]-->

    <!-- es6-shim es6-shim/es6-sham-->
    <!--[if lte IE 11]>
    <script src="/polyfill-lte-ie11.js"></script>
    <![endif]-->
```

- [polyfill-lt-ie10.js](https://raw.githubusercontent.com/fast-flow/support-ie8/master/polyfill-lt-ie10.js)
- [polyfill-lt-ie11.js](https://raw.githubusercontent.com/fast-flow/support-ie8/master/polyfill-lte-ie11.js)

## 其他资源

- [react-ie8](https://github.com/xcatliu/react-ie8)

## 使用特定版本的构建工具

- :+1: `webpack@1.13.2` https://github.com/SamHwang1990/blog/issues/6
- :+1: `karma@1.3.0` https://github.com/karma-runner/karma/issues/2556

## 构建工具兼容配置

- :information_source:  `uglify@2.7.0`之后的版本 设置 `screw-ie8: false` `compress: { warnings: false, screw_ie8: false }, mangle: { screw_ie8: false }, output: { screw_ie8: false }`
- :information_source:  `babel-presets-es2015` 设置 `loose: true` ，避免出现 `Object.defineProperty` *`"presets": [ ["es2015", { "loose": true }] ]`*


## 使用特定版本的第三方包

- :+1: `react@1.14.8` `react@15.*.*` 不兼容IE8
- :+1: `react-router@2.3.0` `2.3.0` 以上版本存在 `Object.defineProperty`
- :+1: `redux@3.*.*`  `redux 4` 不支持IE8 [Redux 4 breaking changes](https://github.com/reactjs/redux/issues/1342)

## 不要使用特定版本的第三方包

- :warning: `react-redux@4.0.1~4.0.3` https://github.com/reactjs/react-redux/issues/227

## 不要使用的第三包

- :warning: `enzyme`
- :warning: `redux-saga` https://github.com/redux-saga/redux-saga/issues/313

## IE Debug

### 禁用内存保护（IE8没有）
![image](https://cloud.githubusercontent.com/assets/3949015/23246656/305ce328-f9d0-11e6-868c-eb5c53698d80.png)

### 禁用崩溃重启
![image](https://cloud.githubusercontent.com/assets/3949015/23246659/3da388ca-f9d0-11e6-9b09-e8d571cd8308.png)

### 找到调试工具

> 吐槽：有时调试工具会出现在屏幕外，导致无法找到。

![image](https://cloud.githubusercontent.com/assets/3949015/23251177/3e85c96c-f9e7-11e6-8b2c-7eb1028fe4d6.png)

### 普通刷新清除不了IE缓存

![image](https://cloud.githubusercontent.com/assets/3949015/23251406/223b18a6-f9e8-11e6-8f2e-1ff475118ad6.png)
