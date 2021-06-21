<template>
  <div class="posts-page">
    <h1 class="posts-page-title">Articles</h1>
    <p class="posts-page-desc">Here you can find my scientific or psychological articles regarding different matters:</p>
  </div>
</template>

<style scoped>
  .posts-page {
    padding: 110px 20px 10px;
  }

  .posts-page-title {
    margin-bottom: 15px;
  }

  .posts-page-desc {
    font-size: 17px;
  }

  @media (max-width: 835px) {

    .posts-page {
      text-align: center;
    }

    .posts-page-title {
      font-size: 25px;
    }

    .posts-page-desc {
      font-size: 15px;
    }
  }
</style>