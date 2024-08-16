<script lang="ts">
  import Form from './lib/Form.svelte';
</script>

<div class="container">
  <h1>Please Login</h1>
  <Form />
</div>

<style lang="scss">
  .container {
    background-color: rgba(0, 0, 0, 0.4);
    padding: 20px 40px;
    border-radius: 5px;

    h1 {
      text-align: center;
      margin-bottom: 30px;
      font-size: 3rem;
    }
  }
</style>
