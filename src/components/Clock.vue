<template>
  <div class="hello">
    <section id="app" class="section">
      <h3 class="title is-3 shadow" v-text="message"></h3>
      <p class="time shadow" v-text="currentTime"></p>
    </section>
  </div>
</template>

<script>
import moment from 'moment';
export default {
  name: 'Clock',
  data () {
    return {
      message: 'Current Time:',
      currentTime: null
    };
  },
  methods: {
    updateCurrentTime() {
      this.currentTime = moment().format('LTS');
    }
  },
  created() {
    this.currentTime = moment().format('LTS');
    setInterval(() => this.updateCurrentTime(), 1 * 1000);
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
section.section {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 140px;
  background: transparent;
}

h3.is-3, p.time {
  color: white;
}

h3.is-3:not(:last-child) {
  margin: 0;
  padding: 0;
}

.time {
  font-size: 7em;
}

.shadow {
  text-shadow: 0 0 15px rgba(100, 100, 100, .35);
}
</style>
