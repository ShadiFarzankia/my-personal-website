<template>
    <div>
        <ul class="navigation-container">
            <li class="navigation-item" @click="closeSideNav">
                <nuxt-link to="/about"
                class="navigation-link">ABOUT ME</nuxt-link>
            </li>
            <li class="navigation-item" @click="closeSideNav">
                <nuxt-link to="books" 
                class="navigation-link">BOOKS</nuxt-link>
            </li>
            <li class="navigation-item" @click="closeSideNav">
                <nuxt-link to="articles"
                class="navigation-link">ARTICLES</nuxt-link>
            </li>
            <li class="navigation-item" @click="closeSideNav">
                <nuxt-link to="experiences"
                class="navigation-link">EXPERIENCES</nuxt-link>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    methods: {
        closeSideNav() {
            this.$emit('closeSideNav', false)
        }
    }
}
</script>

<style scoped>
.navigation-container {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 100%;
    list-style: none;
}

.navigation-item {
    margin-left: 35px;
}

.navigation-link {
    text-decoration: none;
    color: black;
    display: flex;
    font-weight: 600;
    font-size: 13px;
}

.navigation-link:hover,
.navigation-link:active {
    color: darkred;
}

.active-link {
    color: blue;
}

@media (max-width: 855px) {
    
    .navigation-item {
        margin-left: 25px;
        font-size: 11px;
    }
}

@media(max-width: 700px) {
    
    .navigation-container {
        flex-direction: column;  
        align-items: flex-start;  
    }

    .navigation-item {
        margin: 0;
        line-height: 23px;
    }
}

</style>