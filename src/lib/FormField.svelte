<script>
  // @ts-nocheck

  const { label } = $props();
  const letters = (label.at(0).toUpperCase() + label.slice(1)).split('');
</script>

<input id={label} type={label} required placeholder="" /><label for={label}>
  {#each letters as letter, idx (idx)}
    <span style={`transition-delay:${idx * 50}ms`}>{letter}</span>
  {/each}
</label>

<style lang="scss">
  input {
    background-color: transparent;
    border: 0;
    border-bottom: 2px solid #fff;
    display: block;
    width: 100%;
    padding: 15px 0;
    font-size: 18px;
    color: white;

    &:focus {
      outline: 0;
      border-bottom-color: lightblue;
    }
    &:not(:placeholder-shown) {
      border-bottom-color: orange;
    }
    &:valid {
      border-bottom-color: lightgreen;
    }
    &:focus + label span,
    &:not(:placeholder-shown) + label span {
      color: lightblue;
      transform: translateY(-30px);
    }
  }
  label {
    position: absolute;
    top: 15px;
    left: 0;

    span {
      display: inline-block;
      font-size: 18px;
      min-width: 5px;
      transition: 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
    }
  }
</style>
