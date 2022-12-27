<template>
    <div class="container">
        <header>
            <nav class="navbar">
                <NuxtLink class="brand" to="/">Learning Nuxt Products</NuxtLink>
            </nav>
        </header>
        <div>
            <slot />
        </div>
        <Footer />
    </div>
</template>
<style lang="scss" scoped>

        .navbar {
            border-radius: 50px;
            padding: 20px 0;

            .brand {
                font-weight: 700;
                font-size: 1.5rem;
                color: rgb(0, 224, 138);
                text-decoration: none;
            }
        }

        .container {
            width: 1600px;
            margin: 0 auto;
            font-family: "Inter", sans-serif;
            font-size: 16px;
            font-weight: 400;
            line-height: 1.5;
        }
    </style>