<script setup lang="ts">
import {
  Card,
  CardDescription,
  CardHeader,
  CardTitle,
} from "@/components/ui/card";

import { Badge } from "@/components/ui/badge";

enum ProService {
  YES = 1,
  NO = 0,
}

interface ServiceProps {
  title: string;
  pro: ProService;
  description: string;
}

const serviceList: ServiceProps[] = [
  {
    title: "Gearless Motorcycle Training"

    ,
    description:
      "Perfect for beginners who want to learn how to ride gearless scooters or motorcycles. This course covers basic riding skills, balance, and maneuvering techniques to ensure you feel comfortable and safe on the road.",
    pro: 0,
  },
  {
    title: "Manual Car Training",
    description:
      "Specifically designed for those who want to master driving a manual transmission vehicle. This course covers clutch control, gear shifting techniques, and handling various driving situations in a manual car. Gain confidence and skill with our expert instruction",
    pro: 0,
  },
  {
    title: "Motorcycle With Gear Training",
    description: "Designed for those who want to learn how to ride motorcycles with gears. This course includes instruction on gear shifting, clutch control, and handling different road conditions. Our experienced instructors will help you develop the skills needed to ride confidently and safely.",
    pro: 0,
  },
  // {
  //   title: "SEO Optimization",
  //   description: "Lorem ipsum dolor sit amet consectetur.",
  //   pro: 1,
  // },
];
</script>

<template>
  <section id="services" class="container py-24 sm:py-32">
    <h2 class="text-lg text-primary text-center mb-2 tracking-wider">
      Services
    </h2>

    <h2 class="text-3xl md:text-4xl text-center font-bold mb-8">
      Grow Your Business
    </h2>
   
    <div class="grid sm:grid-cols-2 lg:grid-cols-3 gap-4"></div>

    <div class="grid sm:grid-cols-2 lg:grid-cols-2 gap-4 w-full lg:w-[60%] mx-auto">
      <div v-for="{ title, description, pro } in serviceList" :key="title">
        <Card class="bg-muted/60 dark:bg-card h-full relative">
          <CardHeader>``
            <CardTitle>{{ title }}</CardTitle>
            <CardDescription>{{ description }}</CardDescription>
          </CardHeader>
          <Badge v-if="pro === ProService.YES" variant="secondary" class="absolute -top-2 -right-3">PRO</Badge>
        </Card>
      </div>
    </div>
  </section>
</template>
