<script setup lang="ts">

import Separator from "./ui/separator/Separator.vue";
</script>

<template>
  <footer id="footer" class="container py-24 pb-16 sm:py-32 sm:pb-24">
    <div class="p-10 bg-muted/50 dark:bg-card border rounded-2xl">
      <div class="grid grid-cols-2 md:grid-cols-4 xl:grid-cols-6 gap-x-12 gap-y-8">
        <div class="col-span-full xl:col-span-2">
          <a href="#" class="flex font-bold items-center">

            <img src="../assets/Logo.png" alt="" width="50px">
            <h3 class="text-2xl">New Lions DrivingSchool</h3>
          </a>
        </div>

        <div class="flex flex-col gap-2">
          <h3 class="font-bold text-lg">Contact</h3>
          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Github
            </a>
          </div>

          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Twitter
            </a>
          </div>

          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Instagram
            </a>
          </div>
        </div>

        <div class="flex flex-col gap-2">

        </div>

        <div class="flex flex-col gap-2">

        </div>

        <div class="flex flex-col gap-2">
          <h3 class="font-bold text-lg">Socials</h3>
          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Twitch
            </a>
          </div>

          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Discord
            </a>
          </div>

          <div>
            <a href="#" class="opacity-60 hover:opacity-100">
              Dribbble
            </a>
          </div>
        </div>
      </div>

      <Separator class="my-6" />
      <section className="">
        <h3 class="">
          &copy; 2024 Designed and developed by
          <a target="_blank" href="https://adithyan88pb.github.io/Adithyan/"
            className="text-primary transition-all border-primary hover:border-b-2">
            Adithyan PB
          </a>
        </h3>
      </section>
    </div>
  </footer>
</template>
