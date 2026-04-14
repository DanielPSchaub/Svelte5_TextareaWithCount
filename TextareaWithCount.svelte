<script>
  let { name, value="", rows='2', maxlength='200', placeholder='', disabled=false } = $props();
  let currentChars = $state(value.length);
  function getLength(){
    currentChars = value.length;
  }
</script>

<div class="flex flex-col w-full">
  <textarea
    id={name}
    bind:value={value}
    name={name}
    oninput={getLength}
    rows={rows}
    maxlength={maxlength}
    placeholder={placeholder}
    disabled={disabled}
    class=""
  ></textarea>
  <p class="text-xs text-right">{currentChars}/{maxlength}</p>
</div>

<style>
</style>
