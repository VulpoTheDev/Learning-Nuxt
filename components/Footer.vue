<script lang="ts" setup> </script>

<template>
  <footer class="footer">
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
  </footer>
</template>

<style scoped lang="scss">
    .footer {
      ul {
        display: flex;
        flex-direction: row;
        li {
          margin-right: 25px;
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
