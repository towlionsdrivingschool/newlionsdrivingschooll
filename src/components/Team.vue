<script setup lang="ts">
import {
  Card,
  CardContent,
  CardHeader,
  CardTitle,

} from "@/components/ui/card";







</script>

<template>
  <section id="team" class="container lg:w-[75%] py-24 sm:py-32">
    <div class="text-center mb-8">
      <h2 class="text-lg text-primary text-center mb-2 tracking-wider">Team</h2>

      <h2 class="text-3xl md:text-4xl text-center font-bold">
        The Company Dream Team
      </h2>
    </div>

    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-8">
      <Card class="bg-muted/60 dark:bg-card flex flex-col h-full overflow-hidden group/hoverimg">
        <CardHeader class="p-0 gap-0">
          <div class="h-full overflow-hidden">
            <img src="../assets/images/about.jpg" alt=""
              class="w-full aspect-square object-cover saturate transition-all duration-200 ease-linear size-full group-hover/hoverimg:saturate-100 group-hover/hoverimg:scale-[1.01]" />
          </div>
          <CardTitle class="py-6 pb-4 px-6"> Elsy
            <span class="text-primary"> Varghese </span>
          </CardTitle>
        </CardHeader>

        <CardContent>
          CEO-Founder
        </CardContent>

        <!-- <CardFooter class="space-x-4 mt-auto">
          <a v-for="{ name, url } in socialNetworks" key="name" :href="url" target="_blank"
            class="hover:opacity-80 transition-all" :aria-label="`Visit our ${name} page`">
            <component :is="socialIcon(name)" />
          </a>
        </CardFooter> -->
      </Card>
      <Card class="bg-muted/60 dark:bg-card flex flex-col h-full overflow-hidden group/hoverimg">
        <CardHeader class="p-0 gap-0">
          <div class="h-full overflow-hidden">
            <img src="../assets/images/instructotr.jpg" alt=""
              class="w-full aspect-square object-cover saturate transition-all duration-200 ease-linear size-full group-hover/hoverimg:saturate-100 group-hover/hoverimg:scale-[1.01]" />
          </div>
          <CardTitle class="py-6 pb-4 px-6">Anu
            <span class="text-primary"> M Pulluvellil </span>
          </CardTitle>
        </CardHeader>

        <CardContent>
          Instructor
        </CardContent>

        <!-- <CardFooter class="space-x-4 mt-auto">
          <a v-for="{ name, url } in socialNetworks" key="name" :href="url" target="_blank"
            class="hover:opacity-80 transition-all" :aria-label="`Visit our ${name} page`">
            <component :is="socialIcon(name)" />
          </a>
        </CardFooter> -->
      </Card>
      <Card class="bg-muted/60 dark:bg-card flex flex-col h-full overflow-hidden group/hoverimg">
        <CardHeader class="p-0 gap-0">
          <div class="h-full overflow-hidden">
            <img src="../assets/images/bibin .jpg" alt=""
              class="w-full aspect-square object-cover saturate transition-all duration-200 ease-linear size-full group-hover/hoverimg:saturate-100 group-hover/hoverimg:scale-[1.01]" />
          </div>
          <CardTitle class="py-6 pb-4 px-6">Sebastian
            <span class="text-primary"> joseph </span>
          </CardTitle>
        </CardHeader>

        <CardContent>
          TRAINER
        </CardContent>

        <!-- <CardFooter class="space-x-4 mt-auto">
          <a v-for="{ name, url } in socialNetworks" key="name" :href="url" target="_blank"
            class="hover:opacity-80 transition-all" :aria-label="`Visit our ${name} page`">
            <component :is="socialIcon(name)" />
          </a>
        </CardFooter> -->
      </Card>
      <Card class="bg-muted/60 dark:bg-card flex flex-col h-full overflow-hidden group/hoverimg">
        <CardHeader class="p-0 gap-0">
          <div class="h-full overflow-hidden">
            <img src="../assets/Adithyan.jpg" alt=""
              class="w-full aspect-square object-cover  transition-all duration-200 ease-linear size-full group-hover/hoverimg:saturate-100 group-hover/hoverimg:scale-[1.01]" />
          </div>
          <CardTitle class="py-6 pb-4 px-6">Adithyan
            <span class="text-primary"> PB </span>
          </CardTitle>
        </CardHeader>

        <CardContent>
          TRAINER
        </CardContent>

        <!-- <CardFooter class="space-x-4 mt-auto">
          <a v-for="{ name, url } in socialNetworks" key="name" :href="url" target="_blank"
            class="hover:opacity-80 transition-all" :aria-label="`Visit our ${name} page`">
            <component :is="socialIcon(name)" />
          </a>
        </CardFooter> -->
      </Card>
    </div>
  </section>
</template>
