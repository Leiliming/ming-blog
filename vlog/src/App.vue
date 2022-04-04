<template>
  <div>
    <Back></Back>
    <Navigation></Navigation>
    <Content />
    <div id="aplayer"></div>
  </div>
</template>
<script setup lang="js">
import APlayer from "APlayer"; // 引入音乐插件
import "APlayer/dist/APlayer.min.css"; // 引入音乐插件的样式
import Navigation from './components/Navigation/index.vue'
import Back from './components/Back.vue'
import Content from './components/Content/index.vue'
export default {
	name: 'App',
   data() {
    return {
      audio: [
        // 歌曲列表
        {
          title: "secret base~君がくれたもの~",
          artist: "Silent Siren",
          src: "https://moeplayer.b0.upaiyun.com/aplayer/secretbase.mp3",
          pic: "https://moeplayer.b0.upaiyun.com/aplayer/secretbase.jpg",
        },
        {
          name: "周杰伦", // 歌曲名字
          artist: "听妈妈的话", // 歌曲演唱者
          // 歌曲地址（这里用外链地址）
          url: "http://www.170mv.com/kw/antiserver.kuwo.cn/anti.s?rid=MUSIC_138243&response=res&format=mp3|aac&type=convert_url&br=128kmp3&agent=iPhone&callback=getlink&jpcallback=getlink.mp3",
          cover:
            "https://img0.baidu.com/it/u=137179932,574390583&fm=253&fmt=auto&app=138&f=JPEG?w=500&h=332", // 歌曲头像
          lrc: "", // 歌词
          theme: "rgb(127, 218, 180)", // 播放这首歌曲时的主题色
        },
        {
          name: "这一路走来 (cover: 杨宗纬) - 竹之颜",
          artist: " 杨宗纬",
          url: "http://www.170mv.com/kw/antiserver.kuwo.cn/anti.s?rid=MUSIC_150691890&response=res&format=mp3|aac&type=convert_url&br=128kmp3&agent=iPhone&callback=getlink&jpcallback=getlink.mp3",
          cover: 'https://p1.music.126.net/K0-IPcIQ9QFvA0jXTBqoWQ==/109951163636756693.jpg?param=300y300', // prettier-ignore
          lrc: "",
        },
      ],
      info: {
        fixed: true, // 不开启吸底模式
        listFolded: true, // 折叠歌曲列表
        autoplay: true, // 开启自动播放
        preload: "auto", // 自动预加载歌曲
        loop: "all", // 播放循环模式、all全部循环 one单曲循环 none只播放一次
        order: "list", //  播放模式，list列表播放, random随机播放
      },
    };
  },
  mounted() {
    // 初始化播放器
    this.initAudio();
  },
  methods: {
    initAudio() {
      // 创建一个音乐播放器实例，并挂载到DOM上，同时进行相关配置
      const ap = new APlayer({
        container: document.getElementById("aplayer"),
        audio: this.audio, // 音乐信息
        ...this.info, // 其他配置信息
      });
    },
  },
  components:{
    Navigation,
    Content,
	  Back
  }
};
</script>

<style lang="scss">
* {
  cursor: url("./assets/Moony/arrow.cur") 5 5, auto;
  padding: 0;
  margin: 0;
}
//滚动条
</style>
