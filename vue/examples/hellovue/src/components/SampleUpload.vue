<style scoped>

</style>

<template>
  <div>
    <input type="file" @change="handleFileUpload" multiple>
    <button @click="submitFiles">上传文件</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      filesToUpload: []
    };
  },
  methods: {
    handleFileUpload(event) {
      this.filesToUpload = event.target.files;
    },
    submitFiles() {
      const formData = new FormData();
      for (let i = 0; i < this.filesToUpload.length; i++) {
        formData.append('file', this.filesToUpload[i]);
      }

      // Replace with your API endpoint
      const uploadURL = 'http://example.com/upload';

      this.$axios.post(uploadURL, formData, {
        headers: {
          'Content-Type': 'multipart/form-data'
        }
      })
          .then(response => {
            // Handle the response
            console.log(response);
          })
          .catch(error => {
            // Handle error
            console.error(error);
          });
    }
  }
};
</script>
