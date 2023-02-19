<template>
  <main class="userLayout">
    <article class="sidebar">
      <p>Dashboard</p>
      <p>Settings</p>
    </article>
    <section>
      <slot></slot>
    </section>
  </main>
</template>
<style>
.sidebar {
  display: flex;
  flex-direction: column;
}
.userLayout {
  display: flex;
  flex-direction: row;
}
</style>
