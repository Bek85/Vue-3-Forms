<template>
  <label>{{ label }}</label>
  <input :placeholder="label" class="field" />
</template>

<script>
export default {
  name: 'BaseInput',
  props: {
    label: {
      type: String,
      default: ''
    }

  }
}
</script>
