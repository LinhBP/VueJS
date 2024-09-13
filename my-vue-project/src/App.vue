<script>
export default {
  methods: {
    setLanguage(lang) {
      this.$i18n.locale = lang;
    }
  }
};
</script>

<template>
  <div class="container mx-auto p-4">
    <h1 class="text-2xl font-bold">{{ $t('hello') }}</h1>
    <div class="mt-4">
      <button
        class="px-4 py-2 bg-blue-500 text-white rounded mr-2"
        @click="setLanguage('en')"
      >
        EN
      </button>
      <button
        class="px-4 py-2 bg-blue-500 text-white rounded"
        @click="setLanguage('vi')"
      >
        VI
      </button>
    </div>
    <p class="mt-4">{{ $t('language.' + $i18n.locale) }}</p>
  </div>
</template>
