<script>
  export let checked = false;
</script>

<div class="flex gap-x-[10px] justify-center items-center">
  <div class="relative">
    <input id="agree" bind:checked={checked}  type="checkbox" class="peer hidden" required>
    <label for="agree" class="inline-block box-border hover:border-[#8F94B8CC] w-[30px] h-[30px] rounded-[8px] border border-[#3F4363] bg-[#2C2F47] peer-checked:bg-[url('./assets/Checkmark.svg')] peer-checked:bg-center peer-checked:bg-no-repeat"></label>
  </div>
  <p class="text-[#797EA3] pb-[8px] font-[300] text-[15px]">I accept <a href="/" class="text-white underline">Terms and Privacy Policy</a></p>
</div>