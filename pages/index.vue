<template>
    <h1>
    <nav>
      <ul>
        <div><NuxtLink to="/game"><button class="menu" @click="newGame">New Game</button></NuxtLink></div>
        <div><NuxtLink to="/leaderboard"><button class="menu">Leaderboard</button></NuxtLink></div>
        <div><button class="menu" @click="exitGame">Exit</button></div>
      </ul>
    </nav>
    </h1>
</template>

<script setup>

function newGame() {
  console.log("Start new game");
  $post("/menu", "new game")
}

function exitGame() {
  console.log("Exit game");
  $post("/menu", "exit")
}

</script>


<style>
h1 {
  text-align: center;
  margin-top: 4em;
}

.menu {
  height: 50px;
  width: 100px;
}
</style>
