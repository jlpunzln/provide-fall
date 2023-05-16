<template>
  <div>
    <p>I am {{ name }}</p>
  </div>
</template>

<script>
export default {
  name: "PersonalInformation",
  props: {
    name: {
      type: String,
    },
  },
};
</script>
