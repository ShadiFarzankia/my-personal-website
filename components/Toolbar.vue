<template>
    <header class="toolbar">
            <svg class="mobile-only" xmlns="http://www.w3.org/2000/svg" id="Layer_1" enable-background="new 0 0 512 512" height="30px" viewBox="0 0 512 512" width="20px"><g><path d="m464.883 64.267h-417.766c-25.98 0-47.117 21.136-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.013-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/><path d="m464.883 208.867h-417.766c-25.98 0-47.117 21.136-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.013-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/><path d="m464.883 353.467h-417.766c-25.98 0-47.117 21.137-47.117 47.149 0 25.98 21.137 47.117 47.117 47.117h417.766c25.98 0 47.117-21.137 47.117-47.117 0-26.012-21.137-47.149-47.117-47.149z" data-original="#000000" class="active-path" data-old_color="#000000" fill="#C12020"/></g> </svg>
            <div class="logo-container">
                <svg xmlns="http://www.w3.org/2000/svg" width="96px" viewBox="0 0 172.12 66.44"><defs><style>.cls-1{font-size:57px;stroke:#000;font-family:EdwardianScriptITC, Edwardian Script ITC;}.cls-1,.cls-2{stroke-miterlimit:10;}.cls-2{fill:#f15a24;stroke:#f15a24;stroke-width:1px;}</style></defs><title>Asset 1</title><g id="Layer_2" data-name="Layer 2"><g id="Layer_1-2" data-name="Layer 1"><text class="cls-1" transform="translate(0.5 47.24)">Happiness</text><circle class="cls-2" cx="112" cy="26.74" r="4"/></g></g></svg>
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