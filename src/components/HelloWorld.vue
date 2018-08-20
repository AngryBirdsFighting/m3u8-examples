<template>
  <div class="hello">
    <div class="ddd" id="playercontainer"></div>
    <div class="video ddd" style="width: 1000px;height: 600px;"></div>
    <div class="btn">
      <!-- <button @click="play">play</button>
      <button>stop</button> -->
    </div>
  </div>
</template>

<script>
export default {
    name: "HelloWorld",
    data() {
        return {
            msg: "Welcome to Your Vue.js App",
        };
    },
    methods: {
    },
    mounted() {
        // cyberplayer
            var player = cyberplayer("playercontainer").setup({
            width: 680, 
            height: 448, 
            isLive: true, // 必须设置，表明是直播视频
            file: "api/95431869-2278154760-9784600189426728960-2018789548-10057-A-0-1_1200/playlist.m3u8", // <—hls直播地址
            autostart: true,
            stretching: "uniform",
            volume: 100,
            controls: true,
            hls: {
                reconnecttime: 5 // hls直播重连间隔秒数
            },
            ak: "xxxxxxxxxxxxxxxx" // 公有云平台注册即可获得accessKey
        });

        // videojs player
        var videoObject = {
            container: ".video", //“#”代表容器的ID，“.”或“”代表容器的class
            variable: "player", //该属性必需设置，值等于下面的new chplayer()的对象
            autoplay: true, //自动播放
            html5m3u8: true,
            video: "api/95431869-2278154760-9784600189426728960-2018789548-10057-A-0-1_1200/playlist.m3u8" //视频地址
        };
        var player = new ckplayer(videoObject);
    }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.ddd {
    display: inline-block;
    float: left;
}
h1,
h2 {
    font-weight: normal;
}
ul {
    list-style-type: none;
    padding: 0;
}
li {
    display: inline-block;
    margin: 0 10px;
}
a {
    color: #42b983;
}
</style>
