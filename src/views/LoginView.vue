<template>
  <div id="Register">
    <div class="w-full p-6 flex justify-center items-center">
      <div class="w-full max-w-xs">
        <div class="bg-black p-8 shadow rounded mb-6">
          <div class="mb-4">
            <TextInput
                label="email"
                :label-color="false"
                placeholder="example@exaple.com"
                v-model:input="email"
                inputType="text"
                :error="'This is a test error'"
            >
            </TextInput>
          </div>

          <div class="mb-4">
            <TextInput
                label="Password"
                :label-color="false"
                placeholder="password"
                v-model:input="password"
                inputType="password"
                :error="'This is a test error'"
            >
            </TextInput>
          </div>

          <button
              class="
                block
                w-full
                bg-green-500
                text-white
                rounded-sm
                py-3
                text-sm
                tracking-wide
                "
              type="submit"
          >
            Login
          </button>
        </div>

        <p class="text-center text-md text-gray-900">
          Dont have an account yet?
          <router-link to="/register"
                       class="text-blue-500 no-underline hover:underline"
          >
            Register
          </router-link>
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
import TextInput from "@/components/global/TextInput.vue";
import {ref} from "vue";

let email = ref(null)
let password = ref(null)

</script>
