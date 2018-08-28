# m3u8

m3u8 视频直播实例
实例代码在HelloWord.vue 文件中， 分别有videojs player 和 cyberplayer 示例，
m3u8直播视频主要用于移动端直播，为了方便调试就写到了PC端，在PC端播放需要跨域，
解决跨域 ： 在config/index.js 下配置代理即可。
详细API 请参考 https://cloud.baidu.com/doc/MCT/Web-SDK.html  
              https://docs.videojs.com/
示例只在开发环境下使用。             

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
