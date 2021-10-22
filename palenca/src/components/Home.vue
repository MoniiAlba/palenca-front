<template>
  <div class="w-5/6 mx-auto h-full">
    <img src="@/assets/Close.png" class="ml-auto mb-8 cursor-pointer" alt="">
    <img src="@/assets/group-icons.png" class="mx-auto mb-6">
    <p class="leading-9" style="font-size: 22px">
        ACME uses <b>Palenca</b> to connect your bank account
    </p>
    <div class="mx-auto my-6 border border-lightBlue rounded-2xl text-left">
        <img src="@/assets/lock.png" class="" />
        <p class="ml-6">
            Palenca will only be able to read your data
        </p>
        <p class="ml-6">
            ACME Won’t have access to your credentials or be able to perform any action from your account
        </p>
        <a href="https://www.palenca.com/demo" class="cursor-pointer ml-6">
            How Palenca protects your account
        </a>
    </div>
    <section class="absolute bottom-8 w-5/6">
        <button
            class="cursor-pointer w-full rounded-2xl bg-blue-500 h-14 my-4 text-white"
            @click="$emit('nextStep')"
            >
            Continue
        </button>
        <p>By hitting continye you are accepting <a href="https://www.palenca.com/static/pdf/privacy-end-users-spanish.pdf" class="cursor-pointer">
            Palenca’s Privacy Policy</a></p>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Home'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  color: #2772F0;
}
</style>
