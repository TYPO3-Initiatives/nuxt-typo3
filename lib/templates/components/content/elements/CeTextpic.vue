<template>
  <div class="ce-textpic">
    <media-gallery :gallery="gallery">
      <ce-header v-bind="$props" />
      <html-parser :content="bodytext" />
    </media-gallery>
  </div>
</template>
<script>
import baseCe from '../mixins/baseCe'
import MediaGallery from './media/Gallery'
export default {
  name: 'CeTextpic',
  components: {
    MediaGallery
  },
  extends: baseCe,
  props: {
    gallery: {
      type: Object,
      required: true
    },
    bodytext: {
      type: String,
      required: true
    }
  }
}
</script>
