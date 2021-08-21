<template>
  <div class="wrapper">
    <div class="bg-line"></div>
    <div class="sign-up">
      <div class="container">
        <img src="../assets/img/logo.png" alt="">
        <form class="box-shadow" @submit.prevent="signIn">
          <h3>Sign in to your account</h3>
          <div class="input-field">
            <label for="email">Email</label>
            <input type="email" name="email" id="email" v-model="email">
            <small class="err">{{err.email}}</small>
          </div>
          <div class="input-field">
            <div class="pass-flex">
              <label for="password">Password</label>
              <a href="#">Forgot your password</a>
            </div>
            <div class="pass">
              <input type="password" name="password" id="password" v-model="password">
              <img src="../assets/img/eye.png" />
            </div>
            <small class="err">{{err.password}}</small>
          </div>
          <div class="check-field">
            <input type="checkbox" name="signed" id="signed" checked>
            <label for="signed">Stay signed in for a week</label>
          </div>
          <div class="submit">
            <input type="submit" value="Continue" class="btn submit-btn">
            <a href="#">Use single sign-on (SSO) instead</a>
          </div>
        </form>
        <div class="create-acct">
          <p>Don't have an account? <a href="#">Sign up</a></p>
          <div class="pri-pol">
            <p>&copy; Stripe</p> <small class="dot"></small>
            <p>Contact</p> <small class="dot"></small>
            <p>Privacy & terms</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      password: '',
      email: '',
      err: {
          password: '',
          email: '',
        }
    }
  },
  methods: {
    signIn() {
      if (this.password === '') {
        this.err.password = 'Please enter password';
        setTimeout(() => {
          this.err = {}
        }, 2000)
      } 
      if (this.email === '') {
        this.err.email = 'Please provide a valid email address'
        setTimeout(() => {
          this.err = {}
        }, 2000)
      } else if (this.email && this.password) {
        this.email = '';
        this.password = '';
        this.$router.push('/dashboard');
      }
    }
  }
}
</script>

<style>
.wrapper {
  padding-top: 2rem;
  background-color: var(--bg) !important;
  background: url('../assets/img/bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
  background-position: bottom;
  background-attachment: fixed;
}
.sign-up form {
  padding: 2rem 1rem;
  margin: 2rem 0.2rem;
  background: var(--card-bg);
}
.sign-up form h3 {
  color: var(--title-color);
}
.sign-up form .input-field {
  margin: 2rem 0 0;
}
.sign-up form .input-field input {
  display: block;
  margin: 1rem 0;
  width: 100%;
}
.sign-up form .input-field .pass-flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.pass {
  position: relative;
}
.pass img {
  position: absolute;
  top: 50%;
  right: 15px;
  transform: translate(0%, -50%);
}
.sign-up form .check-field {
  margin: 2rem 0;
}
.sign-up form .check-field label {
  margin-left: 0.5rem;
  font-weight: 500;
  color: var(--title-color);
}
.sign-up form .submit {
  text-align: center;
}
.sign-up form .btn {
  display: block;
  width: 100%;
  font-weight: bold;
  font-size: 1rem;
  margin: 0 0 2rem;
  background: var(--btn);
  color: var(--card-bg);
  padding: 1rem;
  cursor: pointer;
}
.sign-up .create-acct {
  margin-bottom: 1.5rem;
}
.sign-up .create-acct p {
  margin: 0 0 1rem;
  font-size: small;
  color: var(--tab-desc);
}
.sign-up .pri-pol {
  display: flex;
  gap: 0.5rem;
  font-weight: bold;
  align-items: center;
}
.sign-up .pri-pol p{
  margin: 0;
  color: var(--copy-tab);
}
.sign-up .pri-pol small {
  height: 2px;
  width: 2px;
  background: var(--copy-tab);
  border-radius: 50%;
}
@media screen and (min-width: 700px) {
  .wrapper {
    position: relative;
  }
  .sign-up {
    width: 700px;
    margin: auto;
    z-index: 10;
    position: relative;
  }
  .sign-up form {
    padding: 3rem;
  }
  .sign-up form h3 {
    font-size: 1.5rem;
  }
  .sign-up .container {
    max-width: 550px;
  }
}
</style>