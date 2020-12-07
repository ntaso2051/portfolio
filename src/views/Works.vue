<template>
  <div class="about">
    <section class="container-fluid">
      <h1>ntaso games</h1>
      <div class="row">
        <div
          class="col-md-6 offset-md-3"
          id="games"
          v-for="(game, index) in games"
          :key="index"
        >
          <div class="zoom">
            <div class="game mx-auto">
              <div>
                <img class="gametitle mx-auto" v-bind:src="game.icon" />
              </div>
              <h3>{{ game.name }}</h3>
              <p>{{ game.description }}</p>
              <a v-bind:href="game.link">遊ぶ</a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Works",
  data() {
    return {
      games: [
        {
          name: "ntasoGameOnline",
          icon: require("@/assets/ngo.png"),
          description:
            "Nodejs製の対戦型オンラインゲーム。Socket.ioとか使って通信してる。サークルのサーバーで動かしてる。",
          link: "http://ntasogameonline.n.trap.show/",
        },
        {
          name: ":amazed_fuzzy:",
          icon: require("@/assets/amazed_fuzzy.png"),
          description:
            "同学科の人たちの間で流行ってる顔文字が主人子で〇ミングスみたいなパズルゲーム。難易度はそこそこ。全部使わなくてもクリアできるらしい。",
          link: "https://ntaso2051.github.io/ntasoGame4/game/",
        },
        {
          name: "A maze",
          icon: require("@/assets/amaze.png"),
          description:
            "穴掘りアルゴリズムを使った迷路ゲーム。実は前作のamazed_fuzzyとa mazeをかけていたりかけていなかったり(激ウマギャグ)。",
          link: "https://ntaso2051.github.io/ntasoGame5/game/",
        },
        {
          name: "モウモウファイト",
          icon: require("@/assets/momo.png"),
          description:
            "Android用の2vs2のオンライン対戦ゲーム。ブログの方に詳しい遊び方とか書いてあるのでそちらを参照。",
          link: "https://trap.jp/post/1149/",
        },
        {
          name: "ElGamal暗号を作るやつ",
          description:
            "これはゲームではないが、セキュリティキャンプで作成した、文字列をElGamal暗号化するものである。こちらもブログに詳しい説明があるので、ブログのリンクを貼っておく。",
          link: "https://trap.jp/post/1167/",
        },
      ],
    };
  },
};
</script>

<style>
#games {
  align-items: center;
}
.game {
  text-align: center;
  width: 800px;
  height: 550px;
  margin-bottom: 40px;
  padding: 20px;
  background-color: lightgray;
  box-shadow: 4px 4px gray;
}
.zoom .game:hover {
  transform: scale(1.1);
  transition-duration: 0.3s;
}
.gametitle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 400px;
  height: 300px;
}
a {
  font-size: 2rem;
}

h3 {
  font-size: 3rem;
  padding: 10px;
}
</style>
