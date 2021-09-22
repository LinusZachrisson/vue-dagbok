<template>
  <div id="addPost">
    <h2>Lägg till nytt inlägg</h2>
    <form @submit="handleSubmit">
      <label>Rubrik:</label>
      <input
        type="text"
        v-model="post.title"
        required
        placeholder="Rubrik"
        id="header"
      />
      <label>Inlägg:</label>
      <textarea v-model="post.content"></textarea>
      <button @submit="handleSubmit">Spara inlägg</button>
    </form>
    <div id="preview">
      <h3>Förhandstitt</h3>
      <p>Rubrik: {{ post.title }}</p>
      <p>Inlägg: {{ post.content }}</p>
    </div>
    <div v-if="submitted">
      <p>Rubrik: {{ post.title }}</p>
      <p>Inlägg: {{ post.content }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Posts",
  data() {
    return {
      post: {
        title: "",
        content: "",
      },
      submitted: false,
    };
  },

  methods: {
    handleSubmit(event) {
      console.log("i userForm submit!");
      event.preventDefault();

      this.submitted = true;
    },
  },
};
</script>

<style>
#addPost * {
  box-sizing: border-box;
}
#addPost {
  margin: 20px auto;
  max-width: 500px;
}
label {
  display: block;
  margin: 20px 0 10px;
}
input[type="text"],
textarea {
  display: block;
  width: 100%;
  padding: 8px;
}
#preview {
  padding: 10px 20px;
  border: 1px dotted black;
  margin: 30px;
}
h3 {
  margin-top: 10px;
}
</style>
