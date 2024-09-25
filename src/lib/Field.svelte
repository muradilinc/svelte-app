<script lang="ts">
  export let value: string = '';
  export let typeInput: 'text' | 'email' | 'tel' = 'text';
  export let valid = false;
  export let rgExp = '';
  export let nameField = '';
  const handleInput = (event: Event) => {
    value = (event.target as HTMLInputElement).value;
  };
</script>

<div class="group">
  <label
    for="name"
    class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">
    {nameField}{valid ? "*" : ""}
  </label>
  <input
    id="name"
    value={value}
    on:input={handleInput}
    class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
    type={typeInput}
    required={valid}
    pattern={rgExp || undefined}
  >
</div>