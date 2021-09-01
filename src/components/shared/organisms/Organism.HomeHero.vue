<template>
  <div class="hero">
    <div class="hero__info">
      <h1 class="hero__info-heading">
        Plannerrify helps teams move work forward.
      </h1>

      <p class="hero__info-description">
        Collaborate, manage projects, and reach new productivity peaks.
        From high rises to the home office,
        the way your team works is unique — accomplish it all with Trello.
      </p>

      <div class="hero__info-signup">
        <input
          v-model="inputValue"
          class="hero__info-input"
        >
        <Button text="Sign up - it's free" />
      </div>
    </div>

    <div class="hero__image" />
  </div>
</template>

<script lang="ts">
import { Button } from '@/components/shared'

export default {
	name: 'OrganismHomeHero',

	components: { Button },

	data () {
		return {
			inputValue: ''
		}
	}
}
</script>

<style scoped lang="scss">
.hero {
  flex: 1;
  display: flex;
  align-items: center;
  max-width: 1024px;
  margin: 24px auto;
  padding: 0 8px;

  &__info {
    flex: 1;
    margin-right: 24px;

    &-heading {
      font-size: 24px;
      font-weight: 900;
    }

    &-description {
      font-weight: 600;
      margin: 32px 0;
    }

    &-signup {
      display: flex;
      justify-content: center;
    }

    &-input {
      flex: 1;
      margin-right: 16px;
    }
  }

  &__image {
    width: 40%;
    height: 100%;
    background: center/contain no-repeat url('https://d2k1ftgv7pobq7.cloudfront.net/meta/p/res/images/spirit/hero/6a3ccd8e5c9a0e8ebea4235d12da6b24/hero.png');

    img {
      max-width: 100%;
    }
  }

  @media only screen and (max-width: 768px) {
    background: center/contain no-repeat url('https://d2k1ftgv7pobq7.cloudfront.net/meta/p/res/images/spirit/hero/6a3ccd8e5c9a0e8ebea4235d12da6b24/hero.png');
    text-align: center;

    &__info {
      padding: 16px 0;
      margin-right: unset;

      &-input {
        display: none;
      }
    }

    &__image {
      display: none;
    }
  }
}
</style>