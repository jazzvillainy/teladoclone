<template>
  <div class="dropdown">
    <div>English</div>
    <div style="border-top: blue solid;">Spanish</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
    };
  },
};
</script>

<style>
.dropdown {
    position: absolute;
    right: 0;
    
}
</style>
