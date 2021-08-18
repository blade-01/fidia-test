<template>
  <div class="wrapper">
    <div class="bg-line"></div>
    <div class="sign-up">
      <div class="container">
        <h1>stripe</h1>
        <form class="box-shadow">
          <h3>Sign in to your account</h3>
          <div class="input-field">
            <label for="email">Email</label>
            <input type="email" name="email" id="email" placeholder="jane.doe@gmail.com">
          </div>
          <div class="input-field">
            <div class="pass-flex">
              <label for="password">Password</label>
              <a href="#">Forgot your password</a>
            </div>
            <input type="password" name="password" id="password" placeholder="Password">
          </div>
          <div class="check-field">
            <input type="checkbox" name="signed" id="signed">
            <label for="signed">Stay signed in for a week</label>
          </div>
          <div class="submit">
            <input type="submit" value="Continue" class="btn">
            <a href="#">Use single sign-on (SSO) instead</a>
          </div>
        </form>
        <div class="create-acct">
          <p>Don't have an account? <a href="#">Sign up</a></p>
          <div class="pri-pol">
            <p>&copy; Stripe</p>
            <p>Contact</p>
            <p>Privacy & terms</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.sign-up form {
  padding: 2rem 1rem;
  margin: 2rem 0.2rem;
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
.sign-up form .check-field {
  margin: 2rem 0;
}
.sign-up form .check-field label {
  margin-left: 0.5rem;
}
.sign-up form .submit {
  text-align: center;
}
.sign-up form .btn {
  display: block;
  width: 100%;
  font-weight: bold;
  margin: 0 0 2rem;
}
.sign-up .create-acct p {
  margin: 0 0 1rem;
}
.sign-up .pri-pol {
  display: flex;
  gap: 0.5rem;
}
@media screen and (min-width: 700px) {
  .wrapper {
    position: relative;
  }
  .sign-up {
    background: rgba(0, 0, 0, 0.2);
    width: 700px;
    margin: auto;
    z-index: 10;
    position: relative;
  }
  .sign-up form {
    padding: 3rem;
    background: #f4f4f4;
  }
  .sign-up .container {
    max-width: 500px;
  }
  .bg-line {
    position: absolute;
    top: 50%;
    left: 0%;
    /* transform: translate(0%, -50%); */
    transform: rotate(-15deg);
    width: 100%;
    height: 20px;
    background: blue;
  }
}
</style>