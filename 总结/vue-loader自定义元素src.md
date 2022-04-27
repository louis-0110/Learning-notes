```js

  chainWebpack: config => {
    config.resolve.alias
      // 第一个参数：别名 第二个参数：路径
      .set('components', resolve('src/components'))
      .set('assets', resolve('src/assets'))
      .set('commonjs', resolve('src/commonjs'))
      .set('views', resolve('src/views'))
    // .set('network', resolve('src/network'))

    config.module
      .rule('vue')
      .use('vue-loader')
      .loader('vue-loader')
     .tap(options => {
        return {
          ...options,
           //配置自定义元素资源打包
          transformAssetUrls: {
            video: ['src', 'poster'],
            source: 'src',
            img: 'src',
            image: ['xlink:href', 'href'],
            use: ['xlink:href', 'href'],
            'lottie-player': 'src'
          }
        }
      })
  },
```

