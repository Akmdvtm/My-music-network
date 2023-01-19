<template>
  <div class="container max-w-4xl mx-auto flex mt-4">
    <div class="w-1/3">
      <img class="w-full rounded-lg h-auto shadow-lg"
           src="https://via.placeholder.com/500"
           alt="profile pic">
    </div>
    <div class="w-full pl-4">
      <div class="flex">
        <div class="w-1/2">
          <h1 class="text-2xl md:text-4xl text-left text-gray-900">
            Tima Akhmedov
          </h1>
          <span class="text-md text-gray-700">
              <i><b>Astana, KZ</b></i>
          </span>
        </div>
        <div class="w-1/2">
          <RouterLinkButton
              btnText="Edit Profile"
              color="green"
              url="account/edit-profile"
          >
          </RouterLinkButton>
        </div>
      </div>
      <ProfileInfoSection></ProfileInfoSection>
      <ProfileAboutSection></ProfileAboutSection>
    </div>
  </div>
  <SongsSection></SongsSection>
  <YoutubeVideoSection></YoutubeVideoSection>
</template>

<script setup>
import ProfileInfoSection from "@/components/partials/profile/ProfileInfoSection.vue";
import ProfileAboutSection from "@/components/partials/profile/ProfileAboutSection.vue";
import RouterLinkButton from "@/components/global/RouterLinkButton.vue";
import SongsSection from "@/components/partials/profile/SongsSection.vue";
import YoutubeVideoSection from "@/components/partials/profile/YoutubeVideoSection.vue";


</script>

<style lang="scss" scoped>

</style>