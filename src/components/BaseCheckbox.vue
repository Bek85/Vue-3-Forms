<template>
  <input class="field" />
  <label v-if="label">{{ label }}</label>
</template>

<script>
export default {
  name: 'BaseCheckbox',
  props: {
    label: {
      type: String,
      default: ''
    }
  }
}
</script>
