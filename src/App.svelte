<script lang="ts">
  import Fields from './lib/Fields.svelte';
  import { FlatToast, ToastContainer } from 'svelte-toasts';
</script>

<main>
  <ToastContainer placement="bottom-right" let:data={data}>
    <FlatToast data={data}/>
  </ToastContainer>
  <div class="flex justify-center items-center h-screen flex-col mx-[10px]">
    <h1 class="text-white text-[55px] font-[500] text-center my-[20px]">Hello</h1>
    <Fields/>
  </div>
</main>

