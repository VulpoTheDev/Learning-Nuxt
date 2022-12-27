<template>
  <div class="container">
    <header>
      <Navbar />
    </header>
    <div>
      <slot />
    </div>
  </div>
</template>

<style lang="scss" scoped>
    .container {
      width: 1600px;
      margin: 0 auto;
      font-family: "Inter", sans-serif;
      font-size: 16px;
      font-weight: 400;
      line-height: 1.5;
    }
  </style>