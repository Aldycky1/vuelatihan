<template>
  <div class="">
    <input
      class="form-check-input"
      v-on:click="done"
      type="checkbox"
      value=""
      :id="tugasSaya.id"
    />
    <label
      class="form-check-label item"
      :class="{ 'item-completed': tugasSaya.isDone }"
      :for="tugasSaya.id"
    >
      {{ tugasSaya.deskripsi }}
    </label>
  </div>
</template>

<script>
export default {
  name: "ItemTugas",
  props: ["tugasSaya"],
  methods: {
    done: function() {
      this.tugasSaya.isDone = true;
    },
  },
};
</script>

<style scoped></style>
