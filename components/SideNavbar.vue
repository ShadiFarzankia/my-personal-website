<template>
    <div>
        <svg class="mobile-only" @click="showSideNav" xmlns="http://www.w3.org/2000/svg" id="Layer_1" enable-background="new 0 0 512 512" height="30px" viewBox="0 0 512 512" width="20px"><g><path d="m464.883 64.267h-417.766c-25.98 0-47.117 21.136-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.013-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/><path d="m464.883 208.867h-417.766c-25.98 0-47.117 21.136-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.013-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/><path d="m464.883 353.467h-417.766c-25.98 0-47.117 21.137-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.012-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/></g> </svg>
        <div class="navbar-container" v-if="show">
            <div class="backdrop-container" @click="hideSideNav"></div>
            <div class="sidedrawer-container">
                <div class="sidedrawer-header">
                    <svg xmlns="http://www.w3.org/2000/svg" width="96px" viewBox="0 0 172.12 66.44"><defs><style>.cls-1{font-size:57px;stroke:#000;font-family:EdwardianScriptITC, Edwardian Script ITC;}.cls-1,.cls-2{stroke-miterlimit:10;}.cls-2{fill:#f15a24;stroke:#f15a24;stroke-width:1px;}</style></defs><title>Asset 1</title><g id="Layer_2" data-name="Layer 2"><g id="Layer_1-2" data-name="Layer 1"><text class="cls-1" transform="translate(0.5 47.24)">Happiness</text><circle class="cls-2" cx="112" cy="26.74" r="4"/></g></g></svg>
                    <button class="close-btn" @click="hideSideNav">
                        <svg height="15px" viewBox="0 0 365.71733 365" width="15px" xmlns="http://www.w3.org/2000/svg"><g fill="#f44336"><path d="m356.339844 296.347656-286.613282-286.613281c-12.5-12.5-32.765624-12.5-45.246093 0l-15.105469 15.082031c-12.5 12.503906-12.5 32.769532 0 45.25l286.613281 286.613282c12.503907 12.5 32.769531 12.5 45.25 0l15.082031-15.082032c12.523438-12.480468 12.523438-32.75.019532-45.25zm0 0"/><path d="m295.988281 9.734375-286.613281 286.613281c-12.5 12.5-12.5 32.769532 0 45.25l15.082031 15.082032c12.503907 12.5 32.769531 12.5 45.25 0l286.632813-286.59375c12.503906-12.5 12.503906-32.765626 0-45.246094l-15.082032-15.082032c-12.5-12.523437-32.765624-12.523437-45.269531-.023437zm0 0"/></g></svg>
                    </button>
                </div>
                <nav class="navigation-list" @click="hideSideNav">
                    <NavigationItems @closeSideNav="show = $event" />
                </nav>
            </div>
        </div>
    </div>
</template>

<script>
export default {
     data() {
        return {
            show: false
        }
    },
    methods: {
        hideSideNav () {
            this.show = false
        },
        showSideNav () {
            this.show = true
        }
    }
}
</script>

<style scoped>
.navbar-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
}
.backdrop-container {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background-color: rgba(220,20,60,.1);
    z-index: 1;
}

.sidedrawer-container {
    width: 100%;
    height: 100vh;
    position: fixed;
    display: flex;
    flex-direction: column;
    transition: transform 0.3s;
    top: 0;
    padding: 20px;
    z-index: 1;
    background-color: white;
    max-width: 300px;
}

.sidedrawer-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.close-btn {
    background-color: unset;
    border: none;
    cursor: pointer;
}

.close-btn:focus {
    outline: none;
}

.navigation-list {
    border-top: 1px solid red;
    padding-top: 25px;
    margin-top: 10px;
}

.open {
    transform: translateX(0);
}

.close {
    transform: translateX(-100%);
}


@media (min-width: 700px) {

    .mobile-only {
        display: none;
    }
}

</style>