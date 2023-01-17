<script>
export default {
  name: "InklineDemo",
  data() {
    return {
      modalVisible: false,
      selected: null,
      options: [
          { id: 1, label: 'Richard Hendricks' },
          { id: 2, label: 'Bertram Gilfoyle' },
          { id: 3, label: 'Dinesh Chugtai' },
          { id: 4, label: 'Jared Dunn' },
          { id: 5, label: 'Erlich Bachman' }
      ],
    };
  },
  methods: {
    toggleColorMode() {
      this.$inkline.toggleColorMode;
    },
  },
}
</script>

<template>
  <i-container>
    <i-row center middle>
      <i-column>
        <i-select
          v-model="selected"
          :options="options"
          placeholder="Choose something.."
        />
      </i-column>
    </i-row>
    <i-row center middle>
      <i-column>
        <i-button
          @click="modalVisible = true"
        >
          Show Modal
        </i-button>
      </i-column>
    </i-row>
    <i-row center middle>
      <i-column>
        <i-button
          @click="toggleColorMode"
        >
          Toggle color mode
        </i-button>
      </i-column>
    </i-row>
  </i-container>
  <!-- modals -->
  <i-modal v-model="modalVisible">
    <template #header> Modal Header </template>
    This is the modal body. Useful information goes here.
    <template #footer> Modal Footer </template>
  </i-modal>
</template>

<style scoped>
</style>
