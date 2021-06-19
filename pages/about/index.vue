<template>
    <div class="main-container">
            <div class="text-container">
                <h1 class="main-title">Hi, I'm Shadi Farzankia.</h1>
                <h2 class="sub-title">Happy Hopeful Girl</h2>
                <div class="par-container">
                    <p class="par-box">
                        I'm a front-end developer who is enthusiastic for learning and experiencing new things.
                        My favorite framework is react and I spend hours in day to learn it deeply.
                    </p>
                    <p class="par-box">
                        I'm also passionate about NY City and I believe in the quoute 
                        <span class="bold-text"> "Work Hard, Dream Big"</span>.
                    </p>
                    <p class="par-box">
                        I'm born in 1994 in Iran. You can discover everything about me below:
                    </p>
                </div>
                <a class="contact-btn">Contact Me</a>
                <div class="social-list">
                <a class="social-list_item" target="_blank">
                    <Twitter />
                </a>
                <a class="social-list_item" target="_blank">
                    <Linkedin />
                </a>
                <a class="social-list_item" target="_blank">
                    <Dribbble />
                </a>
                <a class="social-list_item" target="_blank">
                    <Goodreads />
                </a>
                <a class="social-list_item" target="_blank">
                    <Medium />
                </a>
                </div>
            </div>
            <img class="shadi-img" src={shadiImage} />
        </div>
</template>

<style scoped>
.main-container {
    display: flex;
    justify-content: center;
    min-height: 100vh;
    padding-top: 70px;
}

.shadi-img {
    width: 260px;
    height: 260px;
    margin: 65px 0 0 140px;
    border-radius: 11px;
}

.text-container {
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: center;
}

.main-title {
    font-family: cursive;
    margin-bottom: 40px;
}

.sub-title {
    color: darkred;
    font-size: 20px;
    font-weight: 500;
    margin-bottom: 30px;
}

.bold-text {
    font-weight: bold;
    color: darkred;
}

.par-container {
    margin-bottom: 40px;
}

.par-box {
    max-width: 470px;
    text-align: justify;
    margin-bottom: 15px;
    line-height: 23px;
}

.contact-btn {
    width: 200px;
    height: 36px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: darkred;
    color: white;
    border-radius: 18px;
    margin: 0 auto 20px;
}

.social-list {
    display: flex;
    align-items: center;
    justify-content: center;
}

.social-list_item {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    border: 1px solid black;
    display: inline-flex;
    align-items: center;
    justify-content: center;
    margin-right: 10px;
}

@media (max-width: 835px) {

    .main-container {
        flex-flow: column-reverse;
    }

    .shadi-img {
        margin: 0 auto 55px;
    }

    .main-title {
        margin-bottom: 20px;
        font-size: 21px;
    }

    .sub-title {
        font-size: 17px;
        margin-bottom: 40px;
    }
}
</style>