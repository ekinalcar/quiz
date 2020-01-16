<template>
  <header>
    <b-nav tabs>
      <b-nav-item disabled>
        <b>Fancy Quiz App</b>
      </b-nav-item>
      <b-nav-item disabled>Counter: {{ numCorrect }}/{{ numTotal }}</b-nav-item>
    </b-nav>
  </header>
</template>

<script>
export default {
  props: {
    numCorrect: Number,
    numTotal: Number
  }
};
</script>
