<template>
  <font size="+1">
  <div class="Leaderboard">
  <div v-for="(value, name) in matches.matches">
    entry: {{ name }}
    <div v-for="(entry, name) in value">
      {{ name  }}: {{ entry  }}
    </div>
  </div>
	<nav>
      <ul>
        <NuxtLink to="/"><button class="menu">Back</button></NuxtLink>
      </ul>
	</nav>
  </div>
  </font>
</template>


<script setup>
const {
  data: matches
} = await $get("/leaderboard");

console.log(matches)
</script>

<style>

.Leaderboard {
  text-align: center;
}

</style>
