<template>
  <nav class="navbar">
    <NuxtLink class="brand" to="/">Learning Nuxt</NuxtLink>
    <ul>
      <li>
        <NuxtLink to="/">Home</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/about">About</NuxtLink>
      </li>
      <li>
        <NuxtLink to="/products">Products</NuxtLink>
      </li>
    </ul>
  </nav>
</template>
<style lang="scss" scoped>
    .navbar {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 20px 0;

      .brand {
        font-weight: 700;
        font-size: 1.5rem;
        color: rgb(0, 224, 138);
        text-decoration: none;
      }

      ul {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-around;

        li {
          margin: 0 20px;
          list-style-type: none;

          a {
            text-decoration: none;
            color: white;

          }

          .router-link-exact-active {
            color: rgb(0, 224, 138);
          }
        }
      }
    }
  </style>
