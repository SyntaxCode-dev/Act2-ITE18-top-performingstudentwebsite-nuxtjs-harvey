<script setup lang="ts">
useHead({
  title: 'About | Top Performing Student',
  meta: [{ name: 'description', content: 'Learn about our student achievement website.' }]
})
</script>

<template>
  <section class="page-intro">
    <div class="container">
      <p class="eyebrow">ABOUT US</p>
      <h1>Celebrating student achievement.</h1>
      <p class="hero-description">
        Top Performing Student highlights learners and their academic achievements.
      </p>
      <AppButton label="Explore students" color="#8f1927" href="/" />
    </div>
  </section>

  <section class="section container">
    <div class="info-grid">
      <InfoCard
        title="Our purpose"
        description="Provide recognition for outstanding remarks of students and their academic achievements."
      />
      <InfoCard
        title="Our mission"
        description="To celebrate the hard work and dedication of students, inspiring others to strive for excellence."
      />
      <InfoCard
        title="Our vision"
        description="To create a platform that showcases the achievements of students and encourages a culture of academic excellence."
      />
    </div>
  </section>
</template>
