<template>
  <div class="frameworks__item bg-white mb-5 row rounded" :class="oddEven">
    <div
        class="frameworks__item-image col-12 col-lg-5 p-0 "
        :style="{ background: 'url(' + require(`@/assets/images/${framework.filename}`) + ') center / cover' }"
    >
    </div>
    <div class="frameworks__item-content col-12 col-lg-7 py-3 d-flex flex-column">
      <div class="frameworks__item-title">
        <h3 class="p-0">{{ framework.title }}</h3>
      </div>
      <div class="frameworks__item-description text-muted pb-7">
        {{ framework.description }}
      </div>
      <div class="frameworks__item-btns p-0 d-flex gap-3 mt-auto pb-2">
        <button type="button" class="btn btn-primary">Read more</button>
        <button type="button" class="btn btn-outline-primary">Webinar</button>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "my-frameworks-item",
  props: {
    framework: {
      type: Object,
      required: true,
    }
  },
  computed: {
    oddEven() {
      return this.framework.id % 2 !== 0 ? 'frameworks__item__odd' : 'frameworks__item__even';
    }
  }
}
</script>

<style lang="scss">
.frameworks {
  &__item {
    min-height: 351px;
  }

  &__item__odd {
    flex-direction: row-reverse;

    .frameworks__item-image {
      border-top-right-radius: var(--bs-border-radius);
      border-bottom-right-radius: var(--bs-border-radius);
      @media (max-width: 992px) {
        border-top-left-radius: var(--bs-border-radius);
        border-top-right-radius: var(--bs-border-radius);
        border-bottom-right-radius: 0;
        min-height: 18rem;
      }
    }

    .frameworks__item-content {
      padding-right: 5rem;
      padding-left: 1rem;
      @media (max-width: 992px) {
        padding-right: 2rem;
        padding-left: 2rem;
      }
    }
  }

  &__item__even {
    flex-direction: row;

    .frameworks__item-image {
      border-top-left-radius: var(--bs-border-radius);
      border-bottom-left-radius: var(--bs-border-radius);
      @media (max-width: 992px) {
        border-top-left-radius: var(--bs-border-radius);
        border-top-right-radius: var(--bs-border-radius);
        border-bottom-left-radius: 0;
        min-height: 18rem;
      }
    }

    .frameworks__item-content {
      padding-left: 5rem;
      padding-right: 1rem;
      @media (max-width: 992px) {
        padding-right: 2rem;
        padding-left: 2rem;
      }
    }
  }
}
</style>