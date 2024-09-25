<script lang="ts">
  import Field from './Field.svelte';
  import CheckField from './CheckField.svelte';
  import Button from './Button.svelte';
  import { toasts } from 'svelte-toasts';

  interface FormObj {
    name: string;
    company: string;
    email: string;
    phone: string;
    subject: string;
    message: string;
    agree: boolean;
  }

  const formObj: FormObj = {
    name: '',
    company: '',
    email: '',
    phone: '',
    subject: '',
    message: '',
    agree: false,
  };

  const submitHandler = (event: SubmitEvent) => {
    event.preventDefault();
    const toast = toasts.add({
      title: 'Success!',
      description: 'Данные успешно отправлены.',
      duration: 3000,
      placement: 'top-right',
      type: 'success',
      theme: 'dark',
      onClick: () => {
      },
      onRemove: () => {
      },
    });
  };
</script>

<form on:submit|preventDefault={submitHandler}
      class="bg-[#171929] box-border flex flex-col gap-y-[15px] rounded-[27px] px-[40px] py-[30px] max-w-[390px]">
  <div class="text-center">
    <h2 class="font-[400] text-white text-[18px]">For business enquiries please use the form below</h2>
    <p class="text-[#797EA3] text-[15px] font-[300]">*Required</p>
  </div>
  <Field bind:value={formObj.name} nameField="Name" valid />
  <Field bind:value={formObj.company} nameField="Company" valid />
  <Field bind:value={formObj.email} nameField="Email" typeInput="email" valid />
  <Field bind:value={formObj.phone} nameField="Phone" rgExp="^\d+$" typeInput="tel" valid />
  <Field bind:value={formObj.subject} nameField="Subject" />
  <Field bind:value={formObj.message} nameField="Message" valid />
  <CheckField bind:checked={formObj.agree} />
  <div class="flex justify-center">
    <Button />
  </div>
</form>