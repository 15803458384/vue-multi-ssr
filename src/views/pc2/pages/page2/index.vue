<template>
  <div class="pc2">
    <p>Page2</p>
    <p>ua: {{ ua }}</p>
     <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "page2",
  asyncData(Kit) {
    return Promise.resolve({
      ua: Kit.env.userAgent,
    })
  },
  computed: {
    ua() {
      return this.$store.page2.ua || '';
    }
  }
};
</script>
<style>
.pc2 {
  height: 400px;
  width: 400px;
  text-align: center;
}
</style>