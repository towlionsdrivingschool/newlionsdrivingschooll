<script setup lang="ts">
import { Avatar, AvatarFallback, AvatarImage } from "@/components/ui/avatar";

import {
  Card,
  CardContent,
 
  CardHeader,
  CardTitle,
} from "@/components/ui/card";

import {
  Carousel,
  CarouselContent,
  CarouselItem,
  CarouselNext,
  CarouselPrevious,
} from "@/components/ui/carousel";

import { Star } from "lucide-vue-next";

interface ReviewProps {

  name: string;

  comment: string;
  rating: number;
}

const reviewList: ReviewProps[] = [
  {

    name: "Archana Achu",

    comment:
      "New lions driving school is very good,,, instructor is very co -operative and excellent classes",
    rating: 5.0,
  },
  {

    name: "SANISHA A S",

    comment:
      "The instructors are really knowledgeable and patient. Good experience! ",
    rating: 4.8,
  },

  {

    name: "Anju Rony anna",

    comment:
      "The techniques taught were very useful and the methodology used was just excellent. I enjoyed it thoroughly. Will recommend it without any doubt. Thank you Bibin Ashaan & Sumi chechy.",
    rating: 4.9,
  },
  {

    name: "Athira Kalesh",

    comment:
      "Wonderful experience thank you two lions ... Thank you somuch.",
    rating: 5.0,
  },

];
</script>

<template>
  <section id="testimonials" class="container py-24 sm:py-32">
    <div class="text-center mb-8">
      <h2 class="text-lg text-primary text-center mb-2 tracking-wider">
        Testimonials
      </h2>

      <h2 class="text-3xl md:text-4xl text-center font-bold mb-4">
        Hear What Our 900+ Clients Say
      </h2>
    </div>

    <Carousel :opts="{
      align: 'start',
    }" class="relative w-[80%] sm:w-[90%] lg:max-w-screen-xl mx-auto">
      <CarouselContent>
        <CarouselItem v-for="review in reviewList" :key="review.name" class="md:basis-1/2 lg:basis-1/3">
          <Card class="bg-muted/50 dark:bg-card">
            <CardContent class="pt-6 pb-0">
              <div class="flex gap-1 pb-6">
                <Star class="size-4 fill-primary text-primary" />
                <Star class="size-4 fill-primary text-primary" />
                <Star class="size-4 fill-primary text-primary" />
                <Star class="size-4 fill-primary text-primary" />
                <Star class="size-4 fill-primary text-primary" />
              </div>

              "{{ review.comment }}"
            </CardContent>

            <CardHeader>
              <div class="flex flex-row items-center gap-4">
                <Avatar>
                  <AvatarImage src="https://www.radix-vue.com/logo.svg" alt="@radix-vue" />
                  <AvatarFallback>SV</AvatarFallback>
                </Avatar>

                <div class="flex flex-col">
                  <CardTitle class="text-lg">{{ review.name }}</CardTitle>

                </div>
              </div>
            </CardHeader>
          </Card>
        </CarouselItem>
      </CarouselContent>
      <CarouselPrevious />
      <CarouselNext />
    </Carousel>
  </section>
</template>
