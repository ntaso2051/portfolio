<template>
  <div class="about">
    <section class="container">
      <h1>Introduction</h1>
      <p>
        都内の国立大学生()。某デジタル創作同好会に所属。ぱそこんおままごとをしている。
      </p>
      <h1>Skill</h1>
      <div class="row">
        <div
          class="col-3 col-md-4 mb-5 mb-lg-0"
          v-for="(language, index) in languages"
          :key="index"
        >
          <div class="zoom">
            <div class="lang">
              <div>
                <img class="icon mx-auto" v-bind:src="language.icon" />
              </div>
              <h2>{{ language.name }}</h2>
              <p>{{ language.description }}</p>
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
  name: "About",
  data() {
    return {
      languages: [
        {
          name: "C++",
          icon: require("@/assets/c-plusplus.png"),
          description:
            "競技プログラミングで主に使用している言語。たまにDxライブラリなどを用いてゲーム制作でも使ってる。"
        },
        {
          name: "C#",
          icon: require("@/assets/c-sharp.png"),
          description:
            "Unityで主に使用している言語。たまに競技プログラミングでも使ってる。一番書く機会が多く、多分自分の中で一番書ける言語。"
        },
        {
          name: "Go",
          icon: require("@/assets/gopher.png"),
          description:
            "ISUCONとかで使ってる言語。ゲーム制作でも使えないかと画策している。(鯖書くのnodejsで足りてるし微妙かも。)"
        },
        {
          name: "JavaScript",
          icon: require("@/assets/javascript.png"),
          description: "雰囲気で書いてる言語。なんか知らんけど動くので便利。"
        },
        {
          name: "TypeScript",
          icon: require("@/assets/typescript-icon.png"),
          description:
            "JSを雰囲気でなく書ける言語。今後使っていきたい言語No.1。まだあんま書けない。"
        },
        {
          name: "Vue.js",
          icon: require("@/assets/logo.png"),
          description:
            "このサイト作るのに使ったフレームワーク。booQというWebサービスにちょいちょいPRを出したり出さなかったり。"
        }
      ]
    };
  }
};
</script>

<style>
h1 {
  font-size: 3rem;
  padding: 10px;
}

.icon {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 120px;
  height: 120px;
}

.lang {
  width: 300px;
  height: 350px;
  padding: 20px;
  background-color: lightgray;
  margin-bottom: 20px;
  box-shadow: 4px 4px gray;
}

.zoom .lang:hover {
  transform: scale(1.1);
  transition-duration: 0.3s;
}
</style>
