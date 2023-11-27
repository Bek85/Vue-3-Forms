<template>
  <label v-if="label">{{ label }}</label>
  <select :value="modelValue" class="field">
    <option
      v-for="option in categories"
      :value="option"
      :key="option"
      :selected="option === event.category"
    >
      {{ option }}
    </option>
  </select>
</template>
<script>
export default {
  name: 'BaseSelect',
  props: {
    label: {
      type: String,
      default: ''
    },
    modelValue: {
      type: [String, Number],
      default: ''
    }
  }
}
</script>
