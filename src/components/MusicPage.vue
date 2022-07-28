<template>
  <div class="music_container">
    <header>
      <h1 class="w3-animate-right">Muzyka o tematyce Survivalu</h1>
    </header>
    <main>
      <section class="player w3-animate-left">
        <h2 class="song-title">
          {{ current.title }} - <span>{{ current.artist }}</span>
        </h2>
        <div class="controls">
          <button class="prev" @click="prev">Prev</button>
          <button class="play" v-if="!isPlaying" @click="play">Play</button>
          <button class="pause" v-else @click="pause">Pause</button>
          <button class="next" @click="next">Next</button>
        </div>
      </section>
      <section class="playlist w3-animate-top">
        <h3>Playlista</h3>
        <button v-for="song in songs" :key="song.src" @click="play(song)" :class="(song.src == current.src) ? 'song playing' : 'song'">
          {{ song.title }} - {{ song.artist }}
        </button>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  name: 'MusicPage',
  props: {
    msg: String
  },
data () {
    return {
      current: {},
      index: 0,
      isPlaying: false,
      songs: [
        {
          title: 'Bieszczadzkie anioły',
          artist: 'Stare Dobre Małżeństwo',
          src: require('../assets/music/bieszczadzkie-anioly-stare-dobre-malzenstwo.mp3')
        },
        {
          title: 'Testowy Utwór',
          artist: 'Testowy wykonawca',
          src: require('../assets/music/Black Clover - Opening 3 (HD).mp3')
        },
        {
          title: 'The attack of the dead men',
          artist: 'Sabaton',
          src: require('../assets/music/sabaton-the-attack-of-the-dead-men-official-lyric-video.mp3')
        },
        {
          title: 'Bieszczadzkie anioły',
          artist: 'Stare Dobre Małżeństwo',
          src: require('../assets/music/bieszczadzkie-anioly-stare-dobre-malzenstwo.mp3')
        },
        {
          title: 'Testowy Utwór',
          artist: 'Testowy wykonawca',
          src: require('../assets/music/Black Clover - Opening 3 (HD).mp3')
        },
        {
          title: 'The attack of the dead men',
          artist: 'Sabaton',
          src: require('../assets/music/sabaton-the-attack-of-the-dead-men-official-lyric-video.mp3')
        },
        {
          title: 'Testowy Utwór',
          artist: 'Testowy wykonawca',
          src: require('../assets/music/Black Clover - Opening 3 (HD).mp3')
        },
        {
          title: 'The attack of the dead men',
          artist: 'Sabaton',
          src: require('../assets/music/sabaton-the-attack-of-the-dead-men-official-lyric-video.mp3')
        },
        {
          title: 'Bieszczadzkie anioły',
          artist: 'Stare Dobre Małżeństwo',
          src: require('../assets/music/bieszczadzkie-anioly-stare-dobre-malzenstwo.mp3')
        },
        {
          title: 'Testowy Utwór',
          artist: 'Testowy wykonawca',
          src: require('../assets/music/Black Clover - Opening 3 (HD).mp3')
        },
        {
          title: 'The attack of the dead men',
          artist: 'Sabaton',
          src: require('../assets/music/sabaton-the-attack-of-the-dead-men-official-lyric-video.mp3')
        }
      ],
      player: new Audio()
    }
  },
  methods: {
    play (song) {
      if (typeof song.src != "undefined") {
        this.current = song;
        this.player.src = this.current.src;
      }
      this.player.play();
      this.player.addEventListener('ended', function () {
        this.index++;
        if (this.index > this.songs.length - 1) {
          this.index = 0;
        }
        this.current = this.songs[this.index];
        this.play(this.current);
      }.bind(this));
      this.isPlaying = true;
    },
    pause () {
      this.player.pause();
      this.isPlaying = false;
    },
    next () {
      this.index++;
      if (this.index > this.songs.length - 1) {
        this.index = 0;
      }
      this.current = this.songs[this.index];
      this.play(this.current);
    },
    prev () {
      this.index--;
      if (this.index < 0) {
        this.index = this.songs.length - 1;
      }
      this.current = this.songs[this.index];
      this.play(this.current);
    }
  },
  created () {
    this.current = this.songs[this.index];
    this.player.src = this.current.src;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 70px 0 0;
  font-family: fantasy;
  font-size: 60px;
  text-shadow: 0 0 0.2em #24801a, 0 0 0.2em #e0c708, 0 0 0.2em #24801a;
  transition: 1s;
}
h1:hover
{
  transform: scale(1.05);
  cursor: pointer;
}
h2{

  margin: 20px;
}

a {
  color: #42b983;
}
/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #f1f1f1;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: linear-gradient(to top, #24801a, #37c225);
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: limegreen;
}

body {
	font-family: sans-serif;
}
.music_container
{
  display: flex;
  flex-direction: column;
  align-items: center;
  background: url("../assets/Music_background.jpg");
  background-size: cover;
  min-height: 120vh;
  width: 100vw;
  margin-bottom: -10px;
}
.song-title {
  color: #FFFFFF;
  font-size: 32px;
  font-weight: 700;
  text-transform: uppercase;
  text-align: center;
}
.controls {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px 15px;
}
button {
  appearance: none;
  background: none;
  border: none;
  outline: none;
  cursor: pointer;
}
button:hover {
  opacity: 0.8;
}

.play, .pause {
  font-size: 20px;
  font-weight: 700;
  padding: 15px 25px;
  margin: 0 15px;
  border-radius: 8px;
  color: #FFFFFF;
  background-image: linear-gradient(to left, #24801a, #37c225);
}
.next, .prev {
  font-size: 16px;
  font-weight: 700;
  padding: 10px 20px;
  margin: 0 15px;
  border-radius: 6px;
  color: #FFFFFF;
  background-image: linear-gradient(to right, #24801a, #37c225);
}

.playlist {
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow: auto;
  height: 500px;
}
.playlist h3 {
  color: #FFFFFF;
  font-size: 33px;
  font-weight: 400;
  margin-bottom: 30px;
  text-align: center;
  text-transform: uppercase;
}
.playlist .song {
  color: #FFFFFF;
  width: 40vw;
  padding: 15px;
  font-size: 20px;
  font-weight: 700;
  cursor: pointer;
  background-image: linear-gradient(to right, #24801a, #37c225);
  border-radius: 10px;
}
@media screen and (max-width:900px){
.playlist .song {
  width: 60vw;
}
.music_container {
  height: 1300px;
}

}
@media screen and (max-width:500px){
.playlist .song {
  width: 80vw;
}
.music_container {
  height: 1400px;
}

}


</style>
