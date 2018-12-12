<template>
    <div class="claimWrapper">
      <h1 class="claim">THE UNIVERSE</h1>
      <p class="subclaim">
        Begin your yourney through our amazing galaxy,
      and discover places you never even heard of.
      </p>
      <p class="subclaim">
        Type anythig space-related to start
      </p>
    </div>
</template>

<script>
  export default {
    name: 'Claim.vue',
  };
</script>

<style lang="scss" scoped>
  .claimWrapper {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align: center;
  }

  .claim {
    margin: 0;
    font-size:  50px;
  }

  subclime {
    margin: 20px 0 0 0;
    font-size:  15px;
  }
</style>
