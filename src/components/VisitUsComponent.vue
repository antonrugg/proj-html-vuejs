<template>
<!-- intersection visit our Bakeries -->
  <section class="inter-section">
    <p class="over-title">locations</p>
    <h1 class="title inter">Visit our Bakeries</h1>
  </section>
</template>

<script>
export default {
  name: "VisitUsComponent",
};
</script>

<style lang="scss" scoped>
@import "@/styles/generals.scss";
p {
  font-size: 9px;
  font-weight: 700;
  text-transform: uppercase;
  color: $sub-title-text-color;
  letter-spacing: 1px;
}

h1 {
  font-size: 30px;
  font-weight: bold;
  color: $title-text-color;
  font-family: serif;
}

.inter-section {
  padding-top: 10rem;
  padding-bottom: 4rem;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.title {
  font-size: 44px;
  font-weight: bold;
  color: $title-text-color;
  font-family: serif;
}

.title.inter {
  font-size: 32px;
  margin-top: 1rem;
}
</style>