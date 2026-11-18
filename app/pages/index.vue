<script setup lang="ts">
const students = [
  {
    name: 'Saitama Santos',
    age: 20,
    course: 'Information Technology',
    year: '2nd Year',
    gpa: 1.20,
    email: 'saitama.santos@example.com',
    image: 'images/saitama.jpg'
  },
  {
    name: 'Sakamoto Reyes',
    age: 21,
    course: 'Computer Science',
    year: '3rd Year',
    gpa: 1.3,
    email: 'sakamoto.reyes@example.com',
    image: 'images/sakamoto.jpg'
  },
  {
    name: 'Vegeta Cruz',
    age: 19,
    course: 'Information Systems',
    year: '1st Year',
    gpa: 1.1,
    email: 'vegeta.cruz@example.com',
    image: 'images/vegeta.jpg'
  }
]



useHead({
  title: 'Top Performing Student',
  meta: [{ name: 'description', content: 'Meet our top performing students and view their GPAs.' }]
})
</script>

<template>
  <section class="hero">
    <div class="container hero-content">
      <p class="eyebrow">STUDENT ACHIEVEMENTS</p>
      <h1>Top Performing Student</h1>
      <p class="hero-description">
        Meet our students and celebrate their hard work and academic achievements.
      </p>
      <AppButton label="Meet our students" href="#students" />
    </div>
  </section>

  <section id="students" class="section container">
    <div class="section-heading">
      <div>
        <p class="eyebrow">OUR STUDENTS</p>
        <h2>Top performers</h2>
      </div>
      <span class="student-count">{{ students.length }} students </span>
    </div>

    <div class="student-grid">
      <StudentCard
        v-for="student in students"
        :key="student.email"
        v-bind="student"
      />
    </div>
  </section>

  <section class="section community-section">
    <div class="container">
      <div class="section-heading">
        <div>
          <p class="eyebrow">STUDENT SUCCESS</p>
          <h2>Hard work deserves recognition</h2>
        </div>
      </div>
      <div class="info-grid">
        <InfoCard
          title="Learn"
          description="Discover the interests and achievements that make every student unique."
        />
        <InfoCard
          title="Connect"
          description="Celebrate a welcoming community where students can share their stories."
        />
        <InfoCard
          title="Grow"
          description="Find inspiration in the goals and ideas of fellow students."
        />
      </div>
    </div>
  </section>
</template>
