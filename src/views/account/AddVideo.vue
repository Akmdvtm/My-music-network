<template>
  <div id="AddVideo" class="container mx-auto max-w-4xl pt-20 px-6">
    <div class="text-gray-900 text-xl">Add Youtube Video</div>
    <div class="bg-green-500 w-full h-1 mb-4"></div>
    <TextInput
        class="mb-6"
        label="Title"
        placeholder="cool new song"
        v-model:input="title"
        inputType="text"
        :error="'This is a test error'"
    ></TextInput>
    <TextInput
        class="mb-2"
        label="Video URL"
        placeholder="2VnYXKwneUQ"
        v-model:input="videoCode"
        inputType="text"
        :error="'This is a test error'"
    ></TextInput>
    <SubmitFormButton
        btnText="Add Video"
    ></SubmitFormButton>
  </div>
</template>
<script setup>
import TextInput from "@/components/global/TextInput.vue";
import SubmitFormButton from "@/components/global/SubmitFormButton.vue";
</script>