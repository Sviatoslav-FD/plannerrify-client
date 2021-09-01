<template>
  <div class="header">
    <p class="header__name">
      Plannerrify
    </p>

    <Button
      text="Log in"
      mode="outlined"
      class="header__login-btn"
    />
  </div>
</template>

<script lang="ts">
import { Button } from '@/components/shared'

export default {
	name: 'OrganismHomeHeader',

	components: { Button }
}
</script>

<style scoped lang="scss">
.header {
  display: flex;
  align-items: center;
  background-color: #ececec;
  padding: 8px;

  &__name {
    text-align: start;
    flex: 1;
    font-size: 24px;
    font-weight: 900;
  }
}
</style>