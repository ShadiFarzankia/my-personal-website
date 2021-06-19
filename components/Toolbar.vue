<template>
    <header class="toolbar">
            <!-- <OpenMenu class="mobile-only" onClick={props.opened} /> -->
            <div class="logo-container">
                <!-- <Logo className="logo" /> -->
                <span class="logo-desc desktop-only">This is what my friends call me!</span>
            </div>
            <nav class="desktop-only">
                <NavigationItems />
            </nav>
        </header>
</template>

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
}
</style>