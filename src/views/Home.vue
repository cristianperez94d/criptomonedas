<template>
  <div>
    <bounce-loader :loading="isLoading" :color="'#fbbf24'" :size="'250px'"></bounce-loader>
    <table-comp v-if="!isLoading" :assets="assets" />
  </div>
</template>

<script>
import BounceLoader from 'vue-spinner/src/BounceLoader.vue'
import api from '@/api'
import TableComp from '@/components/TableComp';

export default {
  name: 'Home',
  components: { TableComp , BounceLoader },
  
  data() {
    return {
      isLoading: false,
      assets: []
    }
  },

  created() {
    this.isLoading = true;
    api.getAssets()
    .then(assets => (this.assets = assets))
    .finally( ()=>this.isLoading = false );
  }

};
</script>
