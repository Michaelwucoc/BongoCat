<script setup lang="ts">
import { convertFileSrc } from '@tauri-apps/api/core'
import { resolveResource } from '@tauri-apps/api/path'
import { openPath } from '@tauri-apps/plugin-opener'
import { Button, Select, SelectOption } from 'ant-design-vue'
import { onMounted, ref } from 'vue'
import { useI18n } from 'vue-i18n'

import ProListItem from '@/components/pro-list-item/index.vue'
import { useLocale } from '@/composables/useLocale'

// Tauri API

// Reactive để lưu icon path
const languageIcon = ref('')

/**
 * Lấy icon PNG từ assets/locales và convert sang file://
 */
async function loadLanguageIcon() {
  const path = await resolveResource('assets/locales/languages.svg')
  languageIcon.value = convertFileSrc(path)
}

/**
 * Mở thư mục chứa file ngôn ngữ trong Explorer/Finder
 */
async function openLocalesFolder() {
  const localesPath = await resolveResource('assets/locales')
  await openPath(localesPath)
}

onMounted(() => {
  loadLanguageIcon()
})

const { t } = useI18n()
const { generalStore, locales } = useLocale()
</script>

<template>
  <ProListItem :title="t('general.languages.title')">
    <img
      v-if="languageIcon"
      class="h-5 w-5 cursor-pointer"
      :src="languageIcon"
      :title="t('general.languages.customize')"
      @click="openLocalesFolder"
    >
    <div class="flex flex-1 items-center justify-end gap-3">
      <div class="flex items-center justify-end gap-1">
        <div class="text-xs text-gray-400">
          {{ t('general.languages.customize') }}
        </div>
        <Button
          class="flex items-center gap-1"
          @click="openLocalesFolder"
        >
          <span>{{ t('general.languages.openFolder') }}</span>
          <i class="i-iconamoon:link-external-bold text-4" />
        </Button>
      </div>

      <Select
        v-model:value="generalStore.locale"
        style="width: 150px"
      >
        <SelectOption
          v-for="loc in locales"
          :key="loc.code"
          :value="loc.code"
        >
          {{ loc.name }}
        </SelectOption>
      </Select>
    </div>
  </ProListItem>
</template>
