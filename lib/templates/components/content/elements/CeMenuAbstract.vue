<template>
  <menu-pages v-bind="$props" class="ce-menu-abstract">
    <template #link="{ link }">
      <html-parser
        v-if="link.data && link.data.abstract"
        :content="link.data.abstract"
      />
    </template>
  </menu-pages>
</template>
<script>
import MenuPages from './CeMenuPages'
export default {
  name: 'CeMenuAbstract',
  components: {
    MenuPages
  },
  extends: MenuPages
}
</script>
