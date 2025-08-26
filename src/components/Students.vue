<template>
  <section>
    <h2>Students</h2>
    <ul>
      <li v-for="(n, idx) in names" :key="'n-'+idx">{{ n }}</li>
    </ul>

    <div style="margin: 12px 0;">
      <button @click="showList = !showList">
        {{ showList ? "Hide" : "Show" }} Detailed List
      </button>
    </div>

    <ul v-if="showList">
      <li
        v-for="(s, idx) in students"
        :key="'s-'+idx"
        :class="{ highlight: s.score >= 90 }"
      >
        {{ s.name }} — Score: {{ s.score }}
      </li>
    </ul>

    <p>Passing Students: {{ passingCount }}</p>
  </section>
</template>

<script>
export default {
  name: "Students",
  data() {
    return {
      names: ["Joe", "Marie", "Jemwaks", "David", "Nonoy"],

      showList: true,
      students: [
        { name: "Elyn",   score: 90 },
        { name: "Lyka",     score: 100 },
        { name: "Thea", score: 60 },
      ],
    };
  },
  computed: {
    passingCount() {
      return this.students.filter(s => s.score >= 70).length;
    },
  },
};
</script>

<style>
.highlight {
  color: green;
  font-weight: bold;
}
</style>
