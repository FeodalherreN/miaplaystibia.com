<template>
  <div class="player-wrapper d-none d-md-block">
    <div class="player">
      <img class="player-background" src="../assets/psp.png" />
      <div class="twitchplayer" id="twitch-embed"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TwitchPlayer',
  mounted() {
    this.startStream();
  },
  methods: {
    startStream() {
      /* eslint-disable */
      this.$nextTick(() => {
        let embed = new Twitch.Embed("twitch-embed", {
          width: 520,
          height: 292,
          channel: "lexylou",
          layout: "video",
          autoplay: false,
          parent: ["embed.example.com", "othersite.example.com"]
        });

        embed.addEventListener(Twitch.Embed.VIDEO_READY, () => {
          let player = embed.getPlayer();
          //player.play();
        });
        /* eslint-enable */
      });
    }
  }
}
</script>

<style scoped>
.player-wrapper {
  position: absolute;
  left: 50%;
  top: 50%;
  -webkit-transform: translate(-50%, -50%);
  transform: translate(-50%, -50%);
}

.player {
  position: relative;
}

.player-background {
  width: 1000px;
  position: absolute;
    top: -55px;
    left: -242px;
    z-index: 10;
}

.twitchplayer {
  z-index: 2;
  position: relative;
  z-index: 100;
  border-radius: 25px;
}
</style>
