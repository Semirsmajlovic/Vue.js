<template>
  <div class="tabs">
    <ul class="tabs__header">
      <li v-for="title in tabTitles" :key="title">
        {{ title }}
      </li>
    </ul>
    <slot />
  </div>
</template>

<!-- Here, we will utilize the Composition API to create our slots. -->
<script>
import { ref } from 'vue';

export default {
  // Create our Composition API Setup Method.
  // Since we need access to our component slots, we will pass in arguments.
  // The first argument is the components props, and the second is a content object with three variables.
  // The context will need the components attributes, the emit method to emit events and the components slots.
  // We can access the slots property by destructing the context object.
  setup (props, { slots }) {

    // We need to create a reactive variable that will represent all of our tabs titles.
    // slots.default will give us an array of all the nodes inside a tabs component, which means we will get all of the individual tabs.
    // Since we are only interested in the title field, we can use the arrays.map method and return just the title.
    const tabTitles = ref(slots.default().map((tab) => tab.props.title));

    return {
      tabTitles,
    }
  }
}
</script>
