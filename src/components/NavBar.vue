<template>
    <div class="navbar-fixed">
        <nav class="red lighten-1">
            <div class="nav-wrapper">
                <div class="container">
                    <a href="#" class="brand-logo">Metflix</a>
                    <ul id="nav-mobile" class="right hide-on-med-and-down">
                        <li><router-link to="/">Home</router-link></li>
                        <li><router-link to="/about">About</router-link></li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>

<script>
    export default {
        name: 'NavBar'
    }
</script>

<style scoped>

</style>