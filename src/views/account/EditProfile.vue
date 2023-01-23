<template>
  <div id="EditProfile" class="container max-w-4xl mx-auto pt-20 pb-20 px-6">
    <div class="text-gray-900 text-xl">Edit Profile</div>
    <div class="bg-green-500 w-full h-1"></div>
    <CropperModal
        v-if="showModal"
        :minAspectRatioProp="{width: 8, height:8}"
        :maxAspectRatioProp="{width: 8, height:8}"
        @croppedImageData="setCroppedImageData"
        @showModal="showModal = false"
    ></CropperModal>
    <div class="flex flex-wrap mt-4 mb-6">
      <div class="w-full md:w-1/2 px-3">
        <TextInput
            label="First Name"
            placeholder="Tima"
            v-model:input="firstName"
            inputType="text"
            :error="'This is a test error'"
        ></TextInput>
      </div>
      <div class="w-full md:w-1/2 px-3">
        <TextInput
            label="Last Name"
            placeholder="Akhmedov"
            v-model:input="lastName"
            inputType="text"
            :error="'This is a test error'"
        ></TextInput>
      </div>
    </div>
    <div class="flex flex-wrap mt-4 mb-6">
      <div class="w-full md:w-1/2 px-3">
        <TextInput
            label="Location"
            placeholder="Astana, KZ"
            v-model:input="location"
            inputType="text"
            :error="'This is a test error'"
        ></TextInput>
      </div>
    </div>

    <div class="flex flex-wrap mt-4 mb-6">
      <div class="w-full md:w-1/2 px-3">
        <DisplayCropperButton
            label="Profile Image"
            btnText="Update Profile Image"
            @showModal="showModal = true"
        ></DisplayCropperButton>
      </div>
    </div>

    <div class="flex flex-wrap mt-4 mb-6">
      <div class="w-full md:w-1/2 px-3">
        <CroppedImage
            label="Cropped Image"
            :image="image"
        ></CroppedImage>
      </div>
    </div>

    <div class="flex flex-wrap mt-4 mb-6">
      <div class="w-full md:w-1/2 px-3">
        <TextArea
            label="Description"
            placeholder="Please enter some information"
            v-model="description"
            error=""
        >
        </TextArea>
      </div>
    </div>

    <div class="flex flex-wrap mt-8 mb-6">
      <div class="w-full px-3">
        <SubmitFormButton
            btnText="Update Profile"
        ></SubmitFormButton>
      </div>
    </div>
  </div>
</template>

<script setup>

import TextInput from "@/components/global/TextInput.vue";
import {ref} from "vue";
import DisplayCropperButton from "@/components/global/DisplayCropperButton.vue";
import TextArea from "@/components/global/TextArea.vue";
import SubmitFormButton from "@/components/global/SubmitFormButton.vue";
import CropperModal from "@/components/global/CropperModal.vue";
import CroppedImage from "@/components/global/CroppedImage.vue";

let image = ref(null)
let firstName = ref(null)
let showModal = ref(false)
let lastName = ref(null)
let location = ref(null)
let description = ref(null)

</script>