<template>
  <b-container fluid="sm">
    <h1 class="text-center my-5">Contact</h1>
    <b-row>
      <b-col md="6" offset-md="3">
        <b-form @submit="onSubmit">
          <b-form-group
            id="name"
            label="Name"
            label-for="name-input"
            >
            <b-form-input
              id="name-input"
              v-model="form.name"
              required
              placeholder="Enter your name"
            >
            </b-form-input>
          </b-form-group>
          <b-form-group
            id="email"
            label="Email address:"
            label-for="email-input"
            description="This will just be used to contact you, and will not be shared with anyone."
          >
            <b-form-input
              id="email-input"
              v-model="form.email"
              type="email"
              :state="isValidEmail"
              required
              placeholder="Enter email"
            >
            </b-form-input>
          </b-form-group>
          <b-form-group
            id="message"
            label="Message"
          >
            <b-form-input
              v-model="form.message"
              type="text"
              required
              placeholder="Enter your message"
            >
            </b-form-input>
          </b-form-group>
          <b-button type="submit" variant="primary">Submit</b-button>
        </b-form>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>

export default {
  data() {
    return {
      form: {
        email: '',
        name: '',
        message: '',
      },
    };
  },
  methods: {
    onSubmit(event) {
      event.preventDefault();
      const serverURL = process.env.VUE_APP_API;
      this.axios.post(serverURL, this.form).then((res) => {
        console.log(res);
      }).catch((err) => {
        console.log(err);
      });
    },
    isValidEmail() {
      const re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,24}))$/;
      return re.test(this.form.email);
    },
  },
};
</script>
