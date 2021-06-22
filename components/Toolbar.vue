<template>
    <div class="toolbar">
        <SideNavbar class="mobile-only" :show="isShown" />
        <header class="header">   
            <div class="logo-container">
                <svg xmlns="http://www.w3.org/2000/svg" width="96px" viewBox="0 0 172.12 66.44"><defs><style>.cls-1{font-size:57px;stroke:#000;font-family:EdwardianScriptITC, Edwardian Script ITC;}.cls-1,.cls-2{stroke-miterlimit:10;}.cls-2{fill:#f15a24;stroke:#f15a24;stroke-width:1px;}</style></defs><title>Asset 1</title><g id="Layer_2" data-name="Layer 2"><g id="Layer_1-2" data-name="Layer 1"><text class="cls-1" transform="translate(0.5 47.24)">Happiness</text><circle class="cls-2" cx="112" cy="26.74" r="4"/></g></g></svg>
                <span class="logo-desc desktop-only">This is what my friends call me!</span>
            </div>
            <nav class="desktop-only">
                <NavigationItems />
            </nav>
        </header>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isShown: false
        }
    },
    methods: {
        showSideNav() {
            this.isShown = true
        }
    }
}
</script>

<style scoped>
.toolbar {
    height: 70px;
    width: 100%;
    max-width: 1300px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    padding: 0 33px;
    border-bottom: 1px solid red;
    background-color: white;
}

.header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
}

.logo-container {
    display: flex;
    flex-flow: column;
}

.logo {
    width: 100px;
}

.logo-desc {
    font-size: 12px;
    color: darkred;
    font-family: cursive;
    line-height: 15px;
}

.mobile-only {
    display: none;
}

@media(max-width: 700px) {

    .desktop-only {
        display: none;
    }

    .mobile-only {
        display: block;
    }

    .header {
        justify-content: flex-end;
    }
}
</style>