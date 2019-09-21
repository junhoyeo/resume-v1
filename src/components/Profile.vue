<script>
export default {
  methods: {
    onClickCoffee() {
      const win = window.open('https://toss.im/_m/ZR7jhwxx');
      win.focus();
    },
  },
};
</script>

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
      <div
        class="profile__coffee"
        @click="onClickCoffee"
      >
        <img :src="require('../assets/toss.webp')" />
        <span>커피 사주기</span>
      </div>
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

    @media (max-width: 500px) {
      height: 7rem;
      width: 7rem;
    }
  }

  &__info {
    margin-left: 1rem;
  }

  &__title {
    margin: 0;
    font-size: 3rem;
    font-weight: 900;
    line-height: 1;
    letter-spacing: -1px;

    @media (max-width: 500px) {
      font-size: 2.2rem;
    }
  }

  &__summary {
    margin: 0;
    font-size: 1.2rem;
    font-weight: 300;
  }

  &__coffee {
    cursor: pointer;
    display: inline-flex;
    border: 2px solid #2f5fd2;
    border-radius: 8px;
    justify-content: center;
    align-items: center;
    color: #2f5fd2;
    padding: 0.2rem 0;
    padding-left: .3rem;
    padding-right: .5rem;
    margin-top: .5rem;
    transition: all 2ms;
    font-weight: 500;

    img {
      width: 30px;
      height: 30px;
    }

    span {
      margin-bottom: 3px;
    }

    &:hover,
    &:focus {
      font-weight: 700;
    }
  }
}
</style>
