<script>
import Profile from './components/Profile.vue';
import experience from './data/experience.json';
import outsourcing from './data/outsourcing.json';

export default {
  components: {
    Profile,
  },
  data() {
    return {
      experience,
      outsourcing,
    };
  },
  methods: {
    imageStyle(exp) {
      return {
        // eslint-disable-next-line no-nested-ternary
        width: (exp.full) ? '80%' : (exp.desktop) ? '48%' : '30%',
        border: (exp.noBorder) ? '0' : '1px solid #eaecef',
      };
    },
  },
};
</script>

<template>
  <div class="index">
    <profile />
    <div class="index__content">
      <div class="index__section">
        <h1>Experience <span>경험</span></h1>
        <div class="index__list">
          <div
            class="index__item"
            v-for="(exp, idx) in experience"
            :key="idx"
          >
            <h2>{{ exp.name }}</h2>
            <h3>{{ exp.part }} / {{ exp.event }} / {{ exp.date }}</h3>
            <p>{{ exp.desc }}</p>
            <div
              v-if="exp.images"
              class="index__images"
            >
              <img
                v-for="(img, key) in exp.images"
                :key="key"
                :style="imageStyle(exp)"
                :src="require(`./assets/images/${img}`)"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="index__section">
        <h1>Outsourcing <span>아웃소싱</span></h1>
        <div class="index__list">
          <div
            class="index__item"
            v-for="(out, idx) in outsourcing"
            :key="idx"
          >
            <h2>{{ out.name }}</h2>
            <h3>
              <span v-if="out.part">{{ out.part }}</span>
              <span v-if="out.event">/ {{ out.event }}</span>
              <span v-if="out.date">/ {{ out.date }}</span>
            </h3>
            <p>{{ out.desc }}</p>
            <div
              v-if="out.images"
              class="index__images"
            >
              <img
                v-for="(img, key) in out.images"
                :key="key"
                :style="imageStyle(out)"
                :src="require(`./assets/images/${img}`)"
              />
            </div>
          </div>
        </div>
      </div>
      <!-- <div class="index__section">
        <h1>Education <span>교육</span></h1>
      </div> -->
    </div>
  </div>
</template>

<style lang="scss" scoped>
.index {
  width: 800px;
  background-color: white;

  &__content {
    margin: 0 2rem;
  }

  &__section {

    h1 {
      font-size: 2.5rem;

      span {
        font-size: 1.2rem;
        font-weight: 500;
      }

      @media (max-width: 500px) {
        font-size: 2rem;
      }
    }

    &:last-child {
      margin-bottom: 5rem;
    }
  }

  &__item {
    margin-bottom: 1rem;

    h2, h3, p {
      margin: 0;
    }

    h2 {
      font-size: 1.2rem;
    }

    h3 {
      font-size: 1rem;
      font-weight: 300;
    }

    p {
      color: #383838;
      font-size: .9rem;
    }
  }

  &__images {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    margin-top: 0.5rem;
    margin-bottom: 1.2rem;

    img {
      height: 100%;
      border-radius: 3px;
      user-select: none;
      -webkit-user-drag: none;
    }
  }
}
</style>
