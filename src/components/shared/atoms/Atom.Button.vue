<template>
  <button
    :type="type"
    class="btn"
    :class="{ 'btn-outlined': mode === 'outlined' }"
    @click="onClick"
  >
    {{ text }}
  </button>
</template>

<script lang="ts">
export default {
	name: 'AtomButton',
  
	props: {
		text: {
			type: String,
			default: 'Submit'
		},
		type: {
			type: String,
			default: 'submit'
		},
		/**
     * default
     * outlined
    */
		mode: {
			type: String,
			default: 'default'
		}
	},

	methods: {
		onClick () {
			console.log('Clicked')
		}
	}
}
</script>

<style scoped lang="scss">
// set variables files
.btn {
  background-color: #0065ff;
  color: #fff;
  border: none;
  border-radius: 4px;
  font-size: 16px;
  font-weight: 600;
  --spacer: 8px;
  padding: var(--spacer);
  cursor: pointer;

  &:disabled {
    background-color: #ccc;
    cursor: not-allowed;
  }

  &:hover:not(:disabled) {
    background-color: #0051cc;
  }

  &-outlined {
    background-color: unset;
    color: #0065ff;
    border-radius: unset;
    font-weight: unset;

    &:hover:not(:disabled) {
      background-color: unset;
      color: #0051cc;
      text-decoration: underline;
    }
  }
}
</style>