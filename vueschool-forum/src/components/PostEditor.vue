<template>
  <form action="" @submit.prevent="save">
    <div class="form-group">
        <textarea
          name=""
          id=""
          cols="30"
          rows="10"
          class="form-input"
          v-model="text"
        ></textarea>
    </div>
    <div class="form-actions">
      <button class="btn-blue">Submit Post</button>
    </div>
  </form>
</template>

<script>
    export default {
      data() {
        return {
          text: '',
        };
      },
      props: {
        threadId: {
          required: true,
        },
      },
      methods: {
        save() {
          // For now ids are generated randomly, soon we will get them from a backend
          // (this is just temporary)
          const postId = `greatPost${Math.random()}`;
          const post = {
            text: this.text,
            publishedAt: Math.floor(Date.now() / 1000),
            threadId: this.threadId,
            userId: '7uVPJS9GHoftN58Z2MXCYDqmNAh2',
            '.key': postId,
          };
          this.text = '';
          this.$emit('save', { post });
        },
      },
    };
</script>

<style scoped>

</style>
