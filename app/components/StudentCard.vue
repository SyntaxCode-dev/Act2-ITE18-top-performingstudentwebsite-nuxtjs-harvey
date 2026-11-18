
<script setup lang="ts">
const props = defineProps<{
  name: string
  age: number
  course: string
  year: string
  gpa: number
  email: string
  image: string
}>()
</script>

<template>
  <article class="student-card">
    <div class="student-card-top">

      <img
        :src="image"
        :alt="`${name}'s profile picture`"
        class="student-avatar"
      />

      <span class="student-year">{{ year }}</span>
    </div>

    <h3>{{ name }}</h3>
    <p class="student-course">{{ course }}</p>

    <div class="student-details">
      <span><strong>Age</strong>{{ age }}</span>
      <span><strong>GPA</strong>{{ gpa.toFixed(2) }}</span>
      <a :href="`mailto:${email}`">{{ email }}</a>
    </div>
  </article>
</template>
