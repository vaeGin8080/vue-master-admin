<template>
  <div class="components-container">
    <div>
      <tinymce v-model="content" :height="300" />
    </div>
    <div class="editor-content" v-html="content" />
    <el-button type="primary" @click="submit">提交</el-button>
  </div>
</template>

<script>
import Tinymce from '@/components/Tinymce'

export default {
  name: 'TinymceDemo',
  components: { Tinymce },
  data() {
    return {
      content:  ``
    }
  },
  methods: {
    submit() {
      console.log(this.content)
    }
  }
}
</script>

<style scoped>
.editor-content{
  margin-top: 20px;
}
</style>

