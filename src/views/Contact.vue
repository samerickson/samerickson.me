<template>
  <b-container fluid="sm">
    <h1 class="text-center my-5">Contact</h1>
    <b-row v-if="hasBeenSubmitted">
      <b-col cols="12" lg="6" md="8" offset-lg="3" offset-md="2">
        <h2>Your Message Has been Sent</h2>
        <p>Thanks for reaching out!</p>
        <b-button to="/home" variant="success">Continue</b-button>
      </b-col>
    </b-row>
    <b-row v-else-if="tooManyRequests">
      <b-col cols="12" lg="6" md="8" offset-lg="3" offset-md="2">
        <h2>You have made too many requests</h2>
        <p>Please come back in an hour.</p>
        <b-button to="/home" variant="warning" >Continue</b-button>
      </b-col>
    </b-row>
    <b-row v-else>
      <b-col cols="12" lg="6" md="8" offset-lg="3" offset-md="2">
        <b-form @submit="onSubmit" >
          <b-form-group
            id="name"
            label="Name"
            label-for="name-input"
            >
            <b-form-input
              id="name-input"
              v-model="form.name"
              required
              :state="isValidName()"
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
              :state="isValidEmail()"
              required
              placeholder="Enter email"
            >
            </b-form-input>
          </b-form-group>
          <b-form-group
            id="message"
            label="Message"
          >
            <b-form-textarea
              v-model="form.message"
              type="text"
              required
              rows="6"
              :state="isValidMessage()"
              placeholder="Enter your message"
            >
            </b-form-textarea>
          </b-form-group>
          <b-button :disabled="!isValidEmail()" type="submit" variant="primary">Submit</b-button>
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
      hasBeenSubmitted: false,
      tooManyRequests: false,
    };
  },
  methods: {
    onSubmit(event) {
      if (this.isValidEmail()) {
        console.log('Submitting form');
        event.preventDefault();
        const serverURL = process.env.VUE_APP_API;
        this.axios.post(serverURL, this.form).then((res) => {
          this.hasBeenSubmitted = true;
          console.log(res);
        }).catch((err) => {
          console.log(err);
          this.tooManyRequests = true;
        });
      }
    },
    isValidForm() {
      if (!this.isValidEmail) return false;
      if (!this.isValidName) return false;
      if (!this.isValidMessage) return false;
      return true;
    },
    isValidName() {
      return this.form.name.length > 2 && this.form.name.length < 26;
    },
    isValidMessage() {
      return this.form.message.length > 5 && this.form.message.length < 250;
    },
    isValidEmail() {
      const re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,24}))$/;
      return re.test(this.form.email);
    },
  },
};
</script>
