<template>
    <div @click="$emit('click')" class="cell">
      <span
        v-if="value !== ''"
        :class="{ 'red' : value === 'x', 'green': value === 'o' }"
      >
        {{ value }}
      </span>
    </div>
</template>

<script>
  export default {
    props: {
      value: String,
    },
  }
</script>
<style>


  .cell {
    width: 64px;
    height: 64px;
    border: 2px solid rgb(233,233,233);
    font-size: 42px;

    display: flex;
    align-items: center;
    justify-content: center;
  }

  .red {
    color: rgb(249,116,34);
  }
  .green {
    color: rgb(190,217,72);
  }

  .red,.green {
    position: relative;
    top: -6px;
    font-weight: bold;
    font-size: 48px;
  }
</style>
