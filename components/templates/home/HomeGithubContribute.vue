<template>
  <div class="bg-light-elevatedSurface border-t dark:bg-dark-surface dark:border-dark-border">
    <div class="container mx-auto px-4 py-6">
      <section class="rounded lg:py-6 sm:p-6">
        <!-- why title i18n -->
        <!-- <i18n path="homepage.slack.title" tag="h2" class="text-3xl font-medium pt-10 pb-8 text-center" > </i18n> -->
        <div class="flex justify-between pb-12 sm:py-18">
          <div class="hidden lg:block lg:w-5/12">
            <img src="~/assets/illustrations/developer-github.svg" class="inline-block" />
          </div>
          <div class="w-full lg:w-6/12 xl:w-7/12 lg:mr-12 pt-4 lg:pt-8 text-center lg:text-right">
            <div class="mb-6">
              <!-- <div class="ml-4 "><img src="~/assets/icons/github-2.svg" style="height: 40px" /></div> -->
              <i18n path="homepage.github.title" tag="h3" class="text-2xl font-semibold lg:font-medium lg:text-4xl text-black dark:text-dark-onSurfacePrimary tracking-normal leading-tight" > </i18n>
            </div>
            <i18n
              path="homepage.github.description"
              tag="p"
              class="leading-loose text-light-onSurfaceSecondary dark:text-dark-onSurfaceSecondary"
            >
              <template v-slot:break>
                <br />
              </template>
            </i18n>
            <div class="mt-8">
              <AppButton :variant="null" :href="$config.GithubLink" class="bg-black dark:bg-white text-white dark:text-black hover:bg-gray-900 dark:hover:bg-gray-400 py-3 px-6 text-base" data-cy="slack" >
                <div class="flex">
                  <div class="ml-3">
                    <img v-if="$colorMode.preference === 'light'" src="~/assets/icons/github-3-white.svg" class="w-6 h-6" />
                    <img v-else src="~/assets/icons/github-3.svg" class="w-6 h-6" />
                  </div>
                  {{ $t('homepage.github.button') }}
                </div>
              </AppButton>
            </div>
          </div>
        </div>
      </section>
    </div>
  </div>
</template>

<script>
import IconGroup from '~/components/icons/IconGroup'
export default {
  components: {
    IconGroup
  }
}
</script>
