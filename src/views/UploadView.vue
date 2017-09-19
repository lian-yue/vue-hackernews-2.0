<template>
  <div class="upload-view">
    <ul>
      <li v-for="file in files">
        {{file.name}}
      </li>
    </ul>
    <file-upload
      post-action="/post"
      :multiple="true"
      :thread="3"
      :drop="true"
      :drop-directory="true"
      v-model="files"
      ref="upload">
      Add upload files
    </file-upload>
  </div>
</template>

<script>
import FileUpload from 'vue-upload-component/src'
export default {
  components: { FileUpload },

  data: () => ({
    files: [],
  }),


  title () {
    return 'Upload'
  },
}
</script>
