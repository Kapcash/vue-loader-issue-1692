<template>
  <div class="center">
    <loader>
      <div class="red">
        SHOULD BE RED
      </div>
      <div class="blue">
        IS BLUE
      </div>
    </loader>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';
import Loader from '@/components/Loader.vue';

@Component({
  components: {
    Loader,
  }
})
export default class Page extends Vue {
}
</script>

<style scoped style="css">
.center {
  text-align: center;
}
.red {
  color: red;
}
.blue {
  color: blue;
}
.green {
  color: green;
}
</style>
