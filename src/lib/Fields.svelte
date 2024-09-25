<script lang="ts">
  const formObj = {
    name: '',
    company: '',
    email: '',
    phone: '',
    subject: '',
    message: '',
    agree: false,
  };

  const submitHandler = (event: SubmitEvent) => {
    console.log(formObj);
  };
</script>

<form on:submit|preventDefault={submitHandler}
      class="bg-[#171929] box-border flex flex-col gap-y-[15px] rounded-[27px] px-[40px] py-[30px] max-w-[390px]">
  <div class="text-center">
    <h2 class="font-[400] text-white text-[18px]">For business enquiries please use the form below</h2>
    <p class="text-[#797EA3] text-[15px] font-[300]">*Required</p>
  </div>
  <div class="group">
    <label for="name" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Name*</label>
    <input
      id="name"
      bind:value={formObj.name}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="text"
      required
    >
  </div>
  <div class="group">
    <label for="company" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Company*</label>
    <input
      id="company"
      bind:value={formObj.company}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="text"
      required
    >
  </div>
  <div class="group">
    <label for="email" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Email*</label>
    <input
      id="email"
      bind:value={formObj.email}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="email"
      required
    >
  </div>
  <div class="group">
    <label for="phone" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Phone*</label>
    <input
      id="phone"
      bind:value={formObj.phone}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="tel"
      pattern="^[\\+]?[(]?[0-9]{3}[)]?[-\\s\\.]?[0-9]{3}[-\\s\\.]?[0-9]{4,6}$"
      inputmode="numeric"
      title="Please enter a valid phone number"
      required
    >
  </div>
  <div class="group">
    <label for="subject" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Subject</label>
    <input
      id="subject"
      bind:value={formObj.subject}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="text"
    >
  </div>
  <div class="group">
    <label for="message" class="text-[#797EA3] font-[300] text-[15px] group-focus-within:text-white">Message*</label>
    <input
      id="message"
      bind:value={formObj.message}
      class="bg-[#171929] border-b border-[#3F4363] w-full text-white outline-none focus:border-white"
      type="text"
    >
  </div>
  <div class="flex gap-x-[10px] justify-center items-center">
    <div class="relative">
      <input id="agree" type="checkbox" class="peer hidden" required>
      <label for="agree" class="inline-block box-border hover:border-[#8F94B8CC] w-[30px] h-[30px] rounded-[8px] border border-[#3F4363] bg-[#2C2F47] peer-checked:bg-[url('./assets/Checkmark.svg')] peer-checked:bg-center peer-checked:bg-no-repeat"></label>
    </div>
    <p class="text-[#797EA3] pb-[8px] font-[300] text-[15px]">I accept <a href="#" class="text-white underline">Terms and Privacy Policy</a></p>
  </div>
  <div class="flex justify-center">
    <button
      class="bg-[#2C2F47] box-border text-[18px] text-white font-[400] capitalize px-[50px] py-[12px] rounded-[50px]"
      type="submit">send
    </button>
  </div>
</form>