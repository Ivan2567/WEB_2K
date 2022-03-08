<template>
 <iframe :srcdoc="page" class="frame" id="frame"></iframe>
</template>
<script lang="ts">
export default {
  props: {
    page: [],
  },
};
</script>
<style>
.frame{
    width: 100%;
    height: 600px;
    }
</style>