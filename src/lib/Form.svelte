<script lang="ts">
  import FormField from './FormField.svelte';
</script>

<form>
  <div class="form-control">
    <FormField label="email" />
  </div>
  <div class="form-control">
    <FormField label="password" />
  </div>
  <button class="btn">Login</button>
  <p class="text">Don't have an account? <a href="#">Register</a></p>
</form>

<style lang="scss">
  .form-control {
    position: relative;
    margin: 20px 0 40px;
    max-width: 300px;
  }

  .btn {
    cursor: pointer;
    display: inline-block;
    width: 100%;
    background: lightblue;
    padding: 15px;
    font-family: inherit;
    font-size: 16px;
    border: 0;
    border-radius: 5px;

    &:focus {
      outline: 0;
    }
    &:active {
      transform: scale(0.98);
    }
  }

  .text {
    margin-top: 30px;
  }

  a {
    text-decoration: none;
    color: lightblue;
  }
</style>
