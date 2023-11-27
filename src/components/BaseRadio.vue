<template>
  <input type="radio" />
  <label v-if="label">{{ label }}</label>
</template>

<script>
export default {
  name: 'BaseRadio',
  props: {
    label: {
      type: String,
      default: ''
    }
  }
}
</script>
