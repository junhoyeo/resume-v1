<template>
  <div class="profile">
    <img
      class="profile__image"
      :src="require('../assets/profile.jpeg')"
    />
    <div class="profile__info">
      <h1
        class="profile__title"
      >
        Junho Yeo
      </h1>
      <p class="profile__summary">
        IT를 사용해서 세상에 기여하고자 하는 고등학생입니다.
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Lobster&display=swap');

.profile {
  display: flex;
  flex-direction: row;
  align-items: center;
  margin-top: 1.5rem;
  padding: 1.5rem 2rem;

  &__image {
    height: 9rem;
    width: 9rem;
    border-radius: 50%;
    object-fit: cover;
  }

  &__info {
    margin-left: 1rem;
  }

  &__title {
    margin: 0;
    margin-bottom: 0.5rem;
    font-size: 3rem;
    font-weight: 900;
    letter-spacing: -1px;
  }

  &__summary {
    margin: 0;
    font-size: 1.2rem;
    font-weight: 300;
  }
}
</style>
