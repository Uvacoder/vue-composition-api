<template>
  <div class="home">
    home
    <p ref="p">My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>
import { ref } from "@vue/reactivity";
export default {
  name: "Home",
  setup() {
    const p = ref(null);

    let name = "mario";
    let age = 30;

    const handleClick = () => {
      console.log(p, p.value);
      p.value.classList.add("test");
      p.value.textContent = "AAAAAAAAAAAAAAAAAAAAAAA";
    };

    return { name, age, handleClick, p };
  },
};
</script>
