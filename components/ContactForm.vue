<template>
    <b-form @submit="onSubmit">
        <b-form-group id="input-group-1" label="Your Name:" label-for="input-1">
        <b-form-input
          id="input-1"
          v-model="form.name"
          placeholder="Enter name"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-2"
        label="Email address:"
        label-for="input-2"
        description="We'll never share your email with anyone else."
      >
        <b-form-input
          id="input-2"
          v-model="form.email"
          type="email"
          placeholder="Enter email"
          required
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3">
        <b-form-textarea
            id="textarea"
            v-model="form.message"
            placeholder="Enter something..."
            rows="3"
            max-rows="6"
        ></b-form-textarea>
      </b-form-group>

      <b-button type="submit" variant="primary">Submit</b-button>
    </b-form>
</template>

<script>
  export default {
    data() {
      return {
        form: {
          email: '',
          name: '',
          message: ''
        }
      }
    },
    methods: {
      async onSubmit(event) {
        event.preventDefault()
        let data = await this.$axios.$post('https://formspree.io/f/xdovzobo', this.form)
        console.log(data);
      }
    }
  }
</script>