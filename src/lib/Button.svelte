<script lang="ts">
  export let backGround: string = '#2C2F47';
  export let buttonType: 'submit' | 'button' = 'submit';
</script>
<button
  class={`bg-[${backGround}] box-border text-[18px] text-white font-[400] capitalize px-[50px] py-[12px] rounded-[50px]`}
  type={buttonType}
>
  send
</button>