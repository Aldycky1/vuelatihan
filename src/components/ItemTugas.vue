<template>
  <div class="">
    <input
      class="form-check-input"
      onclick=""
      type="checkbox"
      value=""
      id="defaultCheck1"
    />
    <label
      class="form-check-label item"
      :class="{ 'item-completed': tugasSaya.isDone }"
      for="defaultCheck1"
    >
      {{ tugasSaya.deskripsi }}
    </label>
  </div>
</template>

<script>
export default {
  name: "ItemTugas",
  props: ["tugasSaya"],
};
</script>

<style scoped></style>
