<template>
  <div>
    <h1>Create an event</h1>
    <form>
      <!-- <label>Select a category</label>
      <select v-model="event.category">
        <option
          v-for="option in categories"
          :value="option"
          :key="option"
          :selected="option === event.category"
        >{{ option }}</option>
      </select> -->

      <BaseSelect
        v-model="event.categories"
        label="Select a category"
        :options="categories"
      />

      <h3>Name & describe your event</h3>

      <!-- <label>Title</label>
      <input
        v-model="event.title"
        type="text"
        placeholder="Title"
        class="field"
      > -->
      <BaseInput v-model="event.title" label="Title" type="text" />

      <BaseInput v-model="event.description" label="Description" type="text" />

      <h3>Where is your event?</h3>

      <BaseInput v-model="event.location" label="Location" type="text" />

      <h3>Are pets allowed?</h3>
      <div>
        <!-- <input type="radio" v-model="event.pets" :value="1" name="pets" />
        <label>Yes</label> -->
        <BaseRadio v-model="event.pets" :value="1" label="Yes" name="pets" />
      </div>

      <div>
        <!-- <input type="radio" v-model="event.pets" :value="0" name="pets" />
        <label>No</label> -->
        <BaseRadio v-model="event.pets" :value="0" label="No" name="pets" />
      </div>

      <h3>Extras</h3>
      <!-- <div>
        <input type="checkbox" v-model="event.extras.catering" class="field" />
        <label>Catering</label>
      </div> -->
      <div>
        <BaseCheckbox v-model="event.extras.catering" label="Catering" />
      </div>

      <div>
        <!-- <input type="checkbox" v-model="event.extras.music" class="field" />
        <label>Live music</label> -->
        <BaseCheckbox v-model="event.extras.music" label="Live Music" />
      </div>

      <button class="button -fill-gradient" type="submit">Submit</button>
    </form>
    <pre>{{ event }}</pre>
  </div>
</template>

<script>
// import BaseInput from '@/components/BaseInput.vue'
// import BaseSelect from '@/components/BaseSelect.vue'
// import BaseCheckbox from '@/components/BaseCheckbox.vue'
// import BaseRadio from '@/components/BaseRadio.vue'

export default {
  // components: { BaseInput, BaseSelect, BaseCheckbox, BaseRadio },

  data () {
    return {
      categories: [
        'sustainability',
        'nature',
        'animal welfare',
        'housing',
        'education',
        'food',
        'community'
      ],
      event: {
        category: '',
        title: '',
        description: '',
        location: '',
        pets: 1,
        extras: {
          catering: false,
          music: false
        }
      }
    }
  }
}
</script>
